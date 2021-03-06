---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: MeasureInteger 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 288aee24e0ae6425db35312b560630a6bb9bfc80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843117"
---
# <a name="measureinteger-operation"></a>MeasureInteger 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


퀀텀 레지스터의 콘텐츠를 측정 하 고 정수로 변환 합니다. 측정은 표준 계산 기준, 즉의 eigenbasis을 기준으로 수행 `PauliZ` 됩니다.

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a>입력

### <a name="target--littleendian"></a>대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

작은 endian 인코딩의 퀀텀 레지스터입니다.



## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

측정 된 값을 포함 하는 부호 없는 정수입니다 `target` .

## <a name="remarks"></a>설명

이 작업을 수행 하면 해당 입력 레지스터가 $ \ket{00\cdots 0} $ 상태로 다시 설정 되며 대상 컴퓨터에 다시 배포 하는 데 적합 합니다.

## <a name="see-also"></a>참고 항목

- [MeasureIntegerBE입니다.](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)