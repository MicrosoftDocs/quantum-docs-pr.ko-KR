---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: GetQubitsAvailableToBorrow 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712587"
---
# <a name="getqubitsavailabletoborrow-operation"></a>GetQubitsAvailableToBorrow 작업

네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)

패키지 [](https://nuget.org/packages/)


현재 사용할 수 있는 데 사용할 수 있는 고 비트 수를 반환 합니다.
사용 되지 않은 비트를 포함 합니다. 즉,에 의해 반환 되는의 비트를 포함 `GetQubitsAvailableToUse` 합니다.

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

문에 할당 될 수 있는 값입니다 `borrowing` .
사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.

## <a name="see-also"></a>참고 항목

- [GetQubitsAvailableToUse.](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)