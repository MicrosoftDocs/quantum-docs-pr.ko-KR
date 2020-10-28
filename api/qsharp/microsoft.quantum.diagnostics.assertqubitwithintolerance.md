---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: AssertQubitWithinTolerance 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 3fe4aa739c5e15199401aecb76ef551e52f6dcff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712881"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="a23ad-102">AssertQubitWithinTolerance 작업</span><span class="sxs-lookup"><span data-stu-id="a23ad-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="a23ad-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a23ad-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a23ad-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a23ad-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a23ad-105">`q`지정 된 허용 오차까지 해당 하는 Pauli Z 연산자의 예상 된 eigenstate를 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="a23ad-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="a23ad-106">입력</span><span class="sxs-lookup"><span data-stu-id="a23ad-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="a23ad-107">예상: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="a23ad-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="a23ad-108">에서 예상 하는 것으로 예상 되는 상태는 `Zero` 또는 `One` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a23ad-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="a23ad-109">q: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a23ad-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a23ad-110">상태가 어설션된의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="a23ad-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="a23ad-111">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a23ad-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a23ad-112">예상 결과를 반환할 비트의 측정 확률에 대 한 허용 오차입니다.</span><span class="sxs-lookup"><span data-stu-id="a23ad-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a23ad-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a23ad-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a23ad-114">설명</span><span class="sxs-lookup"><span data-stu-id="a23ad-114">Remarks</span></span>

<span data-ttu-id="a23ad-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> 에서는 $ eigenstates $Z 아닌 임의의 eibit 상태를 어설션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a23ad-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="a23ad-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a23ad-116">See Also</span></span>

- [<span data-ttu-id="a23ad-117">AssertQubitIsInStateWithinTolerance.</span><span class="sxs-lookup"><span data-stu-id="a23ad-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)