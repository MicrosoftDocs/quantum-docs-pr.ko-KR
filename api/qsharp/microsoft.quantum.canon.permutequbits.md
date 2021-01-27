---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: PermuteQubits 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 2fbbe0d99ad1383d77cb08ff6b03bcebd8a1971f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852335"
---
# <a name="permutequbits-operation"></a><span data-ttu-id="90725-102">PermuteQubits 작업</span><span class="sxs-lookup"><span data-stu-id="90725-102">PermuteQubits operation</span></span>

<span data-ttu-id="90725-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="90725-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="90725-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90725-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90725-105">교환 작업을 사용 하 여 Permutes 된 비트</span><span class="sxs-lookup"><span data-stu-id="90725-105">Permutes qubits by using the SWAP operation.</span></span>

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="90725-106">입력</span><span class="sxs-lookup"><span data-stu-id="90725-106">Input</span></span>

### <a name="ordering--int"></a><span data-ttu-id="90725-107">순서 지정: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="90725-107">ordering : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="90725-108">이제 인덱스 i의 새 정렬에 대해 설명 합니다. 여기서는 이제 [i]를 순서 대로 정렬 합니다.</span><span class="sxs-lookup"><span data-stu-id="90725-108">Describes the new ordering of the qubits, where the qubit at index i will now be at ordering[i].</span></span>


### <a name="register--qubit"></a><span data-ttu-id="90725-109">register: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="90725-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="90725-110">작업할의 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="90725-110">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="90725-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="90725-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="90725-112">예</span><span class="sxs-lookup"><span data-stu-id="90725-112">Example</span></span>

<span data-ttu-id="90725-113">지정 된 주문 = [2, 1, 0] 및 등록 $ \ket{\ alpha_0} \ket{\ alpha_1} \ket{\ alpha_2} $ PermuteQubits는 레지스터를 $ \ket{\ alpha_2} \ket{\ alpha_1} \ket{\ alpha_0} $로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="90725-113">Given ordering = [2, 1, 0] and register $\ket{\alpha_0} \ket{\alpha_1} \ket{\alpha_2}$, PermuteQubits changes the register into $\ket{\alpha_2} \ket{\alpha_1} \ket{\alpha_0}$</span></span>

```qsharp
// The following two lines are equivalent
PermuteQubits([2, 1, 0], register);
SWAP(register[0], register[2]);
```