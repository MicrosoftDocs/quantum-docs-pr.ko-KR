---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: GetQubitsAvailableToUse 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201413"
---
# <a name="getqubitsavailabletouse-operation"></a>GetQubitsAvailableToUse 작업

네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


현재 사용할 수 있는 범위의 비트 수를 반환 합니다.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

문에 할당 될 수 있는 값입니다 `using` .
사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.

## <a name="see-also"></a>참고 항목

- [GetQubitsAvailableToBorrow.](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)