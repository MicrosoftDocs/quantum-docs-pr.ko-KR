---
title: 클래식 데이터 로드
description: 사용자 고유의 데이터 집합을 로드 하 여 Microsoft Quantum Development Kit (QDK)로 분류자 모델을 학습 하는 방법을 알아봅니다.
author: geduardo
ms.author: v-edsanc
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.load
no-loc:
- Q#
- $$v
ms.openlocfilehash: cd6fdb6bb33a65ee02ac8c43f40df9abeff9c841
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833696"
---
# <a name="load-and-classify-your-own-datasets"></a>사용자 고유의 데이터 집합 로드 및 분류

이 간단한 자습서에서는 사용자 고유의 데이터 집합을 로드 하 여 QDK (퀀텀 개발 키트)로 분류자 모델을 학습 하는 방법에 대해 알아보겠습니다.

[JSON 파일](https://en.wikipedia.org/wiki/JSON) 등의 표준화 된 serialization 형식을 사용 하 여 데이터를 저장 하는 것이 좋습니다.
이러한 형식은 Python 및 .NET 에코 시스템과 같은 다른 프레임 워크와의 높은 호환성을 제공 합니다.
특히 샘플에서 직접 코드를 복사 하 여 붙여넣을 수 있도록 데이터를 로드 하는 데 템플릿을 사용 하는 것이 좋습니다.

## <a name="template-for-loading-your-datasets"></a>데이터 집합을 로드 하기 위한 템플릿

크기 $N = $2의 학습 데이터 집합 $ (x, y) $가 있다고 가정해 보겠습니다. $x $의 _i $ $x 각 인스턴스에는 $x _ {i1} $, $x _ {i2} $ 및 $x _ {i3} $와 같은 세 가지 기능이 있습니다.
유효성 검사 데이터 집합의 구조가 동일 합니다.
이러한 datsets는 `data.json` 다음과 유사한 파일로 나타낼 수 있습니다.

```json
{
    "TrainingData": {
        "Features": [
            [
                x_11,
                x_12,
                x_13
            ],
            [
                x_21,
                x_22,
                x_23
            ]
        ],
        "Labels": [
            y_1,
            y_2
        ]
    },
    "ValidationData": {
        "Features": [
            [
                xv_11,
                xv_12,
                xv_13
            ],
            [
                xv_11,
                xv_12,
                xv_13
            ]
        ],
        "Labels": [
            yv_1,
            yv_2
        ]
    }
}
```

### <a name="example-using-the-template"></a>템플릿 사용 예

다른 고양이와 강아지의 높이와 가중치가 있는 작은 데이터 집합이 있다고 가정 합니다. 이 데이터 집합은 모델을 학습 하는 데 매우 작지만 데이터 집합 로드 프로세스를 표시 하는 데에는 충분 합니다.

| 높이 (m) | 무게 (kg) | 동물 |
|-----------|------------|--------|
| 0.54      | 30         | Dog    |
| 0.30      | 8          | Cat    |
| 0.91      | 44         | Dog    |
| 0.86      | 31          | Dog    |
| 0.32      | 5         | Cat    |
| 0.25      | 4          | Cat    |

프로세스는.

- 먼저 데이터 집합을 학습 및 유효성 검사로 구분 해야 합니다. 이 경우 학습을 위한 처음 3 개의 샘플 및 유효성 검사를 위한 샘플의 나머지 부분을 수행 하면 됩니다. 일반적으로 학습 데이터에 원치 않는 편향을 방지 하기 위해 무작위로 학습 및 유효성 검사 데이터 집합을 샘플링 하는 것이 좋습니다.
- 두 번째로, 각 클래스에 숫자 레이블을 할당 해야 합니다. 지금은 QML 라이브러리는 이진 분류 문제만 인정 합니다. 따라서 클래스에 레이블 0을 할당 하 `Dog` 고 클래스에 숫자 1을 할당 합니다 `Cat` .
- 마지막으로, 데이터 집합의 데이터를 사용 하 여 템플릿을 채웁니다. 빅 데이터 집합의 경우 특정 데이터 집합에서 템플릿을 자동으로 생성 하는 작은 스크립트를 작성 해야 합니다. 이 스크립트는 데이터 집합의 원본 형식에 따라 달라 집니다.

데이터 집합의 경우 `data.json` 파일은 다음과 같습니다.

```json
{
    "TrainingData": {
        "Features": [
            [
                0.54,
                30
            ],
            [
                0.30,
                8
            ],
            [
                0.91,
                44
            ]
        ],
        "Labels": [
            0,
            1,
            0
        ]
    },
    "ValidationData": {
        "Features": [
            [
                0.86,
                31
            ],
            [
                0.32,
                5
            ]
            [
                0.25,
                4
            ]
        ],
        "Labels": [
            0,
            1,
            1
        ]
    }
}

```

## <a name="loading-the-data"></a>데이터 로드

JSON 파일로 serialize 된 데이터를 사용 하는 경우 선택한 호스트 언어와 함께 제공 되는 JSON 라이브러리를 사용 하 여 로드할 수 있습니다.

### <a name="python"></a>[Python](#tab/tabid-python)

Python은 JSON 직렬화 된 데이터로 작업 하기 위한 [기본 제공 `json` 패키지](https://docs.python.org/3.7/library/json.html) 를 제공 합니다.

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[C#](#tab/tabid-csharp)

.NET Core 플랫폼은 JSON 직렬화 된 데이터로 작업 하기 위한 [ `System.Text.Json` 패키지](https://www.nuget.org/packages/System.Text.Json) 를 제공 합니다.

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="next-steps"></a>다음 단계

이제 고유한 데이터 집합을 사용 하 여 사용자 고유의 실험을 실행할 준비가 되었습니다. 다른 분류자와 데이터 집합을 시도 하 고 결과를 공유 하는 커뮤니티에 기여 하세요.
