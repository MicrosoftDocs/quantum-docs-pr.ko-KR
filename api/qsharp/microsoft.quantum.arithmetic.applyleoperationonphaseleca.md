---
uid: Microsoft.Quantum.Arithmetic.ApplyLEOperationOnPhaseLECA
title: ApplyLEOperationOnPhaseLECA 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyLEOperationOnPhaseLECA
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.phaselittleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.littleendian>.
ms.openlocfilehash: 4762eb17b4c11e46b5b94498b7fc8fd2f855c659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190686"
---
# <a name="applyleoperationonphaseleca-operation"></a>ApplyLEOperationOnPhaseLECA 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


<xref:microsoft.quantum.arithmetic.phaselittleendian>형식의 대상 레지스터에서 등록을 입력으로 사용 하는 작업을 적용 <xref:microsoft.quantum.arithmetic.littleendian> 합니다.

```qsharp
operation ApplyLEOperationOnPhaseLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl), target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>입력

### <a name="op--littleendian--unit--is-adj--ctl"></a>op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl

적용 될 작업입니다.


### <a name="target--phaselittleendian"></a>대상: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

작업이 적용 되는 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

레지스터는를 사용 하 `LittleEndian` 여로 변환 된 <xref:microsoft.quantum.canon.qftle> 다음의 응용 프로그램 후 원래 표현으로 반환 됩니다 `op` .

## <a name="see-also"></a>참고 항목

- [ApplyLEOperationonPhaseLE입니다.](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLE)
- [ApplyLEOperationonPhaseLEA입니다.](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEA)
- [ApplyLEOperationonPhaseLEC입니다.](xref:Microsoft.Quantum.Canon.ApplyLEOperationonPhaseLEC)