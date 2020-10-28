---
uid: Microsoft.Quantum.Chemistry.HTerm
title: HTerm 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTerm
qsharp.summary: Format of data passed from C# to Q# to represent a term of the Hamiltonian. The meaning of the data represented is determined by the algorithm that receives it.
ms.openlocfilehash: 7a18db539e55e4c1086b3d83725e3d4ba87f0117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714869"
---
# <a name="hterm-user-defined-type"></a>HTerm 사용자 정의 형식

네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)

패키지 [](https://nuget.org/packages/)


C #에서 Q #으로 전달 되는 데이터의 형식으로 Hamiltonian의 용어를 나타냅니다.
표시 되는 데이터의 의미는 해당 데이터를 수신 하는 알고리즘에 의해 결정 됩니다.

```qsharp

newtype HTerm = (Int[], Double[]);
```

