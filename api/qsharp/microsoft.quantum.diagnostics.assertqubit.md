---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: AssertQubit 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: fa1f52da5a011cd914a0fda69b78cf5a4fd71e16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712944"
---
# <a name="assertqubit-operation"></a><span data-ttu-id="0a9aa-102">AssertQubit 작업</span><span class="sxs-lookup"><span data-stu-id="0a9aa-102">AssertQubit operation</span></span>

<span data-ttu-id="0a9aa-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="0a9aa-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="0a9aa-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0a9aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0a9aa-105">`q`Eibit가 Pauli Z 연산자의 예상 eigenstate 임을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a9aa-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.</span></span>

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="0a9aa-106">입력</span><span class="sxs-lookup"><span data-stu-id="0a9aa-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="0a9aa-107">예상: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="0a9aa-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="0a9aa-108">에서 예상 하는 것으로 예상 되는 상태는 `Zero` 또는 `One` 입니다.</span><span class="sxs-lookup"><span data-stu-id="0a9aa-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="0a9aa-109">q: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0a9aa-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0a9aa-110">상태가 어설션된의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="0a9aa-110">The qubit whose state is asserted.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0a9aa-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0a9aa-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0a9aa-112">설명</span><span class="sxs-lookup"><span data-stu-id="0a9aa-112">Remarks</span></span>

<span data-ttu-id="0a9aa-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> 에서는 $ eigenstates $Z 아닌 임의의 eibit 상태를 어설션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a9aa-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a9aa-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0a9aa-114">See Also</span></span>

- [<span data-ttu-id="0a9aa-115">AssertQubitIsInStateWithinTolerance.</span><span class="sxs-lookup"><span data-stu-id="0a9aa-115">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)