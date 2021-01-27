---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: ResetAll 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 2b8e7fc0e7881d8c1bd6f14c150476262b7a2b19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849311"
---
# <a name="resetall-operation"></a><span data-ttu-id="91947-102">ResetAll 작업</span><span class="sxs-lookup"><span data-stu-id="91947-102">ResetAll operation</span></span>

<span data-ttu-id="91947-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="91947-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="91947-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="91947-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="91947-105">원하는 비트 배열을 지정 하 고이를 측정 하 여 안전 하 게 해제할 수 있도록 | 0 ⟩ 상태에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="91947-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="91947-106">입력</span><span class="sxs-lookup"><span data-stu-id="91947-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="91947-107">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="91947-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="91947-108">주가 $ \ket $로 다시 설정 될 valbits의 배열입니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="91947-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="91947-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91947-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

