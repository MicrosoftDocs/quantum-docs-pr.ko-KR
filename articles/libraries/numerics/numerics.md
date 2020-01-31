---
title: 숫자 라이브러리 사용 | Microsoft Docs
description: 숫자 라이브러리 사용
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.usage
ms.openlocfilehash: ca24ff60cd9ae5077c7f4bae0012fe1180d7e6d4
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "76821034"
---
# <a name="using-the-numerics-library"></a>숫자 라이브러리 사용

## <a name="overview"></a>개요

숫자 라이브러리는 세 가지 구성 요소로 구성 됩니다.

1. 정수 adder 및 비교 연산자를 사용 하는 **기본 정수 산술 연산**
1. 기본 기능을 기반으로 하는 **상위 수준의 정수 기능** 여기에는 곱하기, 나누기, 역 등이 포함 됩니다.  부호 있는 정수와 부호 없는 정수에 대 한입니다.
1. 고정 소수점 초기화, 더하기, 곱하기, 상호, 다항식 계산 및 측정이 포함 된 **고정 소수점 산술 기능** 입니다.

이러한 모든 구성 요소는 단일 `open` 문을 사용 하 여 액세스할 수 있습니다.
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a>유형

숫자 라이브러리는 다음 형식을 지원 합니다.

1. **`LittleEndian`** : `qArr[0]`에서 최하위 비트를 나타내는 정수를 나타내는 `qArr : Qubit[]`입니다.
1. **`SignedLittleEndian`** : 2의 보수에 저장 된 부호 있는 정수를 나타내는 점을 제외 하 고 `LittleEndian`와 동일 합니다.
1. **`FixedPoint`** : `qArr2 : Qubit[]` 하 고 이진 점 위치 `pos`으로 구성 된 실수를 나타냅니다 .이 숫자는 이진 점 왼쪽의 이진 자릿수를 계산 합니다. `qArr2`는 `SignedLittleEndian`와 동일한 방식으로 저장 됩니다.

## <a name="operations"></a>운영

위의 세 가지 형식 각각에 대해 다양 한 작업을 사용할 수 있습니다.

1. **`LittleEndian`**
    - 더하기
    - 비교
    - 곱하기
    - 제곱
    - 나누기 (나머지 포함)

1. **`SignedLittleEndian`**
    - 더하기
    - 비교
    - 역 모듈로 2의 보수
    - 곱하기
    - 제곱

1. **`FixedPoint`**
    - 기존 값에 대 한 준비/초기화
    - 더하기 (기존 상수 또는 기타 퀀텀 고정 소수점)
    - 비교
    - 곱하기
    - 제곱
    - 짝수 및 홀수 함수를 위한 특수화로 다항식 계산
    - 역 (1/x)
    - 측정 (고전적인 Double)

이러한 각 작업에 대 한 자세한 내용 및 자세한 설명서는 [docs.microsoft.com](https://docs.microsoft.com/quantum) 에서 Q # 라이브러리 참조 문서를 참조 하세요.

## <a name="sample-integer-addition"></a>샘플: 정수 더하기

기본 예로 $ $ \ket x\ket y\maps\ket x\ket {x + y} $ $를 사용 하는 것이 좋습니다. 즉, nstbit 정수 $x $ 및 n-또는 (n + 1)-stbit register $y $를 입력으로 사용 하 고 후자는 sum $ (x + y) $에 매핑되는 연산입니다. $Y $이 $n $ 비트 레지스터에 저장 된 경우 합계는 모듈러스 $2 ^ n $로 계산 됩니다.

퀀텀 개발 키트를 사용 하 여 다음과 같이이 작업을 적용할 수 있습니다.
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        x = LittleEndian(xQubits); // define bit order
        y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a>샘플: 부드러운 함수 계산

퀀텀 컴퓨터에서 $ \sin (x) $와 같은 부드러운 함수를 평가 하려면 ($x $은 퀀텀 `FixedPoint` number) 퀀텀 개발 키트 숫자 라이브러리는 작업 `EvaluatePolynomialFxP` 및 `Evaluate[Even/Odd]PolynomialFxP`를 제공 합니다.

첫 번째 `EvaluatePolynomialFxP`에서는 $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \c9+ a_dx ^ d, $ $ 형식의 다항식을 평가할 수 있습니다. 여기서 $d $는 *각도*를 나타냅니다. 이렇게 하려면 `[a_0,..., a_d]` 다항식 계수 (`Double[]`형식), 입력 `x : FixedPoint` 및 출력 `y : FixedPoint` (처음에는 0)만 필요 합니다.
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
결과 $P (x) = 1 + 2x $는 `yFxP`에 저장 됩니다.

두 번째, `EvaluateEvenPolynomialFxP`및 세 번째 `EvaluateOddPolynomialFxP`는 각각 짝수 및 홀수 함수의 사례에 대 한 특수화입니다. 즉, 짝수/홀수 함수 $f (x) $ 및 $ $ P_ {짝수} (x) = a_0 + a_1 x ^ 2 + a_2 x ^ 4 + \cs+ a_d x ^ {2d}의 경우 $ $ $f (x) $는 $P _ {짝수} (x) $ 또는 $P _ {홀수} (x): = x\cdot P_ {짝수} (x) $에서 각각 합니다.
Q #에서 이러한 두 가지 사례는 다음과 같이 처리할 수 있습니다.
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
이는 $P _ {짝수} (x) = 1 + 2x ^ 2 $를 평가 합니다.
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
$P _ {홀수} (x) = x + 2x ^ 3 $를 평가 합니다.

## <a name="more-samples"></a>추가 샘플

[주 샘플 리포지토리에서](https://github.com/Microsoft/Quantum)더 많은 샘플을 찾을 수 있습니다.

시작 하려면 리포지토리를 복제 하 고 `Numerics` 하위 폴더를 엽니다.

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Numerics
```

그런 다음 샘플 폴더 중 하나에 `cd` 하 고을 통해 샘플을 실행 합니다.

```bash
dotnet run
```
