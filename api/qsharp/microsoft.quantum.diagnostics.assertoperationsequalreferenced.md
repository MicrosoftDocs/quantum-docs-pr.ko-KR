---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: AssertOperationsEqualReferenced 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: a3e8791321b4f2ca1885dffeb92c7b13e5491a32
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712958"
---
# <a name="assertoperationsequalreferenced-operation"></a><span data-ttu-id="f261f-102">AssertOperationsEqualReferenced 작업</span><span class="sxs-lookup"><span data-stu-id="f261f-102">AssertOperationsEqualReferenced operation</span></span>

<span data-ttu-id="f261f-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f261f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f261f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f261f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f261f-105">두 작업이 지정 된 경우는 모든 입력 상태에 대해 동일 하 게 작동 한다는 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="f261f-106">이 어설션은 Choi – Jamiołkowski isomorphism를 사용 하 여 두 entangled 레지스터의를 사용 하는 것으로 어설션을 줄이는 방법으로 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-106">This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers.</span></span>
<span data-ttu-id="f261f-107">따라서이 작업은 테스트 되는 각 작업에 대 한 단일 호출만 필요 하지만 할당 해야 하는 것은 두 배입니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-107">Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated.</span></span>
<span data-ttu-id="f261f-108">이 어설션을 사용 하면 예를 들어, 작업의 최적화 된 버전이 naive 구현에 동일 하 게 작동 하거나, 비 퀀텀 입력 범위에서 작동 하는 작업이 알려진 사례에 동의 하는 경우를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-108">This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.</span></span>

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="f261f-109">입력</span><span class="sxs-lookup"><span data-stu-id="f261f-109">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="f261f-110">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f261f-110">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f261f-111">각 작업에 전달할 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-111">Number of qubits to pass to each operation.</span></span>


### <a name="actual--qubit--unit"></a><span data-ttu-id="f261f-112">actual: [bit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f261f-112">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f261f-113">테스트할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-113">Operation to be tested.</span></span>


### <a name="expected--qubit--unit-adj"></a><span data-ttu-id="f261f-114">예상: 이상 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span><span class="sxs-lookup"><span data-stu-id="f261f-114">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="f261f-115">테스트 중인 작업의 예상 동작을 정의 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-115">Operation defining the expected behavior for the operation under test.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f261f-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f261f-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f261f-117">설명</span><span class="sxs-lookup"><span data-stu-id="f261f-117">Remarks</span></span>

<span data-ttu-id="f261f-118">이 작업을 수행 하려면 예상 되는 동작을 모델링 하는 작업이 adjointable 해야 합니다. 따라서 역은 대상 레지스터 에서만 수행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-118">This operation requires that the operation modeling the expected behavior is adjointable, so that the inverse can be performed on the target register alone.</span></span>
<span data-ttu-id="f261f-119">공식적으로는 이러한 요구 사항을 완화 하는 바꾸기 작업을 지정할 수 있지만,이 경우에는 바꾸기 작업이 임의의 퀀텀 작업에 대해 일반적으로 실제로 realizable 되지 않으므로이 옵션으로 여기에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f261f-119">Formally, one can specify a transpose operation, which relaxes this requirement, but the transpose operation is not in general physically realizable for arbitrary quantum operations and thus is not included here as an option.</span></span>