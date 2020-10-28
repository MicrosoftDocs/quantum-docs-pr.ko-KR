---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: ResetAll 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 00b7c0f508d76fb0f5b46c7ec00c0718469365a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711411"
---
# <a name="resetall-operation"></a><span data-ttu-id="a4e60-102">ResetAll 작업</span><span class="sxs-lookup"><span data-stu-id="a4e60-102">ResetAll operation</span></span>

<span data-ttu-id="a4e60-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a4e60-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a4e60-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a4e60-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a4e60-105">원하는 비트 배열을 지정 하 고이를 측정 하 여 안전 하 게 해제할 수 있도록 | 0 ⟩ 상태에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e60-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a4e60-106">입력</span><span class="sxs-lookup"><span data-stu-id="a4e60-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="a4e60-107">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a4e60-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a4e60-108">주가 $ \ket $로 다시 설정 될 valbits의 배열입니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="a4e60-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a4e60-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a4e60-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

