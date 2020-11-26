---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdder
title: ApplyInnerTTKAdder 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdder
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 1de0248066aec531d78130703414067603ffd34d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191009"
---
# <a name="applyinnerttkadder-operation"></a>ApplyInnerTTKAdder 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


RippleCarryAdderTTK 작업에 대 한 내부 더하기 함수를 구현 합니다. 이 작업은 전체 adder를 생성 하는 외부 작업과 conjugated 된 내부 작업입니다.

```qsharp
operation ApplyInnerTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="xs--littleendian"></a>xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian cobit summand 입력을 RippleCarryAdderTTK에 첫 번째 정수를 등록 합니다.


### <a name="ys--littleendian"></a>작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

LittleEndian cobit는 두 번째 정수 summand 입력을 RippleCarryAdderTTK에 등록 합니다.


### <a name="carry--qubit"></a>운반: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)

Xored은 합계의 가장 중요 한 비트를 사용 하 여 수행 됩니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

지정 된 제어 작업을 통해 작업의 대칭 및 상호 취소를 사용 하 여 모든 작업에 컨트롤을 추가 하는 기본 구현을 개선 합니다.

## <a name="references"></a>참조 항목

- Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "퀀텀 추가 회로 및 무제한 팬 아웃", 퀀텀 정보 및 계산, Vol. 10, 2010.
  https://arxiv.org/abs/0910.2530