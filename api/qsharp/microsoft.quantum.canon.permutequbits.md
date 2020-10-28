---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: PermuteQubits 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 0f4d8819d5b08f4d5370f8fdc407b2eb2a3e5f21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715660"
---
# <a name="permutequbits-operation"></a><span data-ttu-id="1cb7b-102">PermuteQubits 작업</span><span class="sxs-lookup"><span data-stu-id="1cb7b-102">PermuteQubits operation</span></span>

<span data-ttu-id="1cb7b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1cb7b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1cb7b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1cb7b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1cb7b-105">교환 작업을 사용 하 여 Permutes 된 비트</span><span class="sxs-lookup"><span data-stu-id="1cb7b-105">Permutes qubits by using the SWAP operation.</span></span>

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1cb7b-106">입력</span><span class="sxs-lookup"><span data-stu-id="1cb7b-106">Input</span></span>

### <a name="ordering--int"></a><span data-ttu-id="1cb7b-107">순서 지정: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1cb7b-107">ordering : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1cb7b-108">이제 인덱스 i의 새 정렬에 대해 설명 합니다. 여기서는 이제 [i]를 순서 대로 정렬 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb7b-108">Describes the new ordering of the qubits, where the qubit at index i will now be at ordering[i].</span></span>


### <a name="register--qubit"></a><span data-ttu-id="1cb7b-109">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1cb7b-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1cb7b-110">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb7b-110">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1cb7b-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1cb7b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

