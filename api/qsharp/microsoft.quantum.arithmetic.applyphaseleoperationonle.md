---
uid: Microsoft.Quantum.Arithmetic.ApplyPhaseLEOperationOnLE
title: ApplyPhaseLEOperationOnLE 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyPhaseLEOperationOnLE
qsharp.summary: Applies an operation that takes a <xref:microsoft.quantum.arithmetic.littleendian> register as input on a target register of type <xref:microsoft.quantum.arithmetic.phaselittleendian>.
ms.openlocfilehash: d94fdb55e051e76dd518eff14b80d1a24516bf8a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843673"
---
# <a name="applyphaseleoperationonle-operation"></a>ApplyPhaseLEOperationOnLE 작업

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


<xref:microsoft.quantum.arithmetic.littleendian>형식의 대상 레지스터에서 등록을 입력으로 사용 하는 작업을 적용 <xref:microsoft.quantum.arithmetic.phaselittleendian> 합니다.

```qsharp
operation ApplyPhaseLEOperationOnLE (op : (Microsoft.Quantum.Arithmetic.PhaseLittleEndian => Unit), target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>입력

### <a name="op--phaselittleendian--unit"></a>op: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) 

적용 될 작업입니다.


### <a name="target--littleendian"></a>대상: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

작업이 적용 되는 레지스터입니다.



## <a name="output--unit"></a>출력: [단위](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>설명

레지스터는를 사용 하 `PhaseLittleEndian` 여로 변환 된 <xref:microsoft.quantum.canon.qftle> 다음의 응용 프로그램 후 원래 표현으로 반환 됩니다 `op` .

## <a name="see-also"></a>참고 항목

- [ApplyPhaseLEOperationonLEA입니다.](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [ApplyPhaseLEOperationonLEA입니다.](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLEA)
- [ApplyPhaseLEOperationonLECA입니다.](xref:Microsoft.Quantum.Canon.ApplyPhaseLEOperationonLECA)