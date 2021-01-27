---
uid: Microsoft.Quantum.Simulation.Unitary
title: 단일 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: Unitary
qsharp.summary: Represents evolution under a unitary operator.
ms.openlocfilehash: f148b59d2445f964fc0332e2010571a0ace2d4ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858391"
---
# <a name="unitary-user-defined-type"></a>단일 사용자 정의 형식

네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)

패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)


단일 연산자의 진화를 나타냅니다.

```qsharp

newtype Unitary = ((Qubit[] => Unit is Adj + Ctl));
```

