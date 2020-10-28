---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlaceCompBasis
title: AssertOperationsEqualInPlaceCompBasis 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlaceCompBasis
qsharp.summary: Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis. This is a necessary, but not sufficient, condition for the equality of two unitaries.
ms.openlocfilehash: 3275680f86ca2a178c7f044b97d226fe41c3186c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712965"
---
# <a name="assertoperationsequalinplacecompbasis-operation"></a><span data-ttu-id="84469-102">AssertOperationsEqualInPlaceCompBasis 작업</span><span class="sxs-lookup"><span data-stu-id="84469-102">AssertOperationsEqualInPlaceCompBasis operation</span></span>

<span data-ttu-id="84469-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="84469-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="84469-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="84469-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="84469-105">`givenU` `expectedU` 계산 단위의 벡터 에서만 작업의 동작을 확인 하 여 작업이 지정 된 입력 크기에 대 한 작업과 같은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="84469-105">Checks if the operation `givenU` is equal to the operation `expectedU` on the given input size  by checking the action of the operations only on the vectors from the computational basis.</span></span>
<span data-ttu-id="84469-106">이는 두 unitaries의 같음에 대 한 필수 조건 이지만 충분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84469-106">This is a necessary, but not sufficient, condition for the equality of two unitaries.</span></span>

```qsharp
operation AssertOperationsEqualInPlaceCompBasis (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="84469-107">입력</span><span class="sxs-lookup"><span data-stu-id="84469-107">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="84469-108">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="84469-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="84469-109">작업이 수행 하 고 작동 하는 $n $의 수입니다 `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="84469-109">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="84469-110">givenU: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84469-110">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="84469-111">검사 될 $ 이상 비트 $n에 대 한 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="84469-111">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="84469-112">Adj Unit [()](xref:microsoft.quantum.lang-ref.qubit)=> [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84469-112">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="84469-113">비교할 $로 비트 $n에 대 한 참조 연산 `givenU` 입니다.</span><span class="sxs-lookup"><span data-stu-id="84469-113">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="84469-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84469-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

