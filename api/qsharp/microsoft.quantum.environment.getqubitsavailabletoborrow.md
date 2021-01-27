---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: GetQubitsAvailableToBorrow 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: f2294fadb9c10d800b7a743fbfe0810f36f18516
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853240"
---
# <a name="getqubitsavailabletoborrow-operation"></a>GetQubitsAvailableToBorrow 작업

네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


현재 사용할 수 있는 데 사용할 수 있는 고 비트 수를 반환 합니다.

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

사용할 수 있으며 문의 일부로 할당 되지 않는 원하는 비트 수입니다 `borrowing` .
사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.

## <a name="see-also"></a>참고 항목

- [GetQubitsAvailableToUse.](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)