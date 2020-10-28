---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: GetQubitsAvailableToUse 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712580"
---
# <a name="getqubitsavailabletouse-operation"></a>GetQubitsAvailableToUse 작업

네임 스페이스: [Microsoft 퀀텀. 환경](xref:Microsoft.Quantum.Environment)

패키지 [](https://nuget.org/packages/)


현재 사용할 수 있는 범위의 비트 수를 반환 합니다.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>출력: [Int](xref:microsoft.quantum.lang-ref.int)

문에 할당 될 수 있는 값입니다 `using` .
사용 중인 대상 컴퓨터에서이 정보를 제공 하지 않으면이 `-1` 반환 됩니다.

## <a name="see-also"></a>참고 항목

- [GetQubitsAvailableToBorrow.](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)