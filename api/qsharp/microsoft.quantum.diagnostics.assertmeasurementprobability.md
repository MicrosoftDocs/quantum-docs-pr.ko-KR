---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: AssertMeasurementProbability 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 032b9224ad728f0637596668c2928a889deeba55
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202365"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="5a071-102">AssertMeasurementProbability 작업</span><span class="sxs-lookup"><span data-stu-id="5a071-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="5a071-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="5a071-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="5a071-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="5a071-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="5a071-105">지정 된 Pauli의 지정 된 비트를 측정 하는 어설션은 특정 허용 범위 내에서 지정 된 확률을 포함 하는 지정 된 결과를 갖게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a071-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5a071-106">입력</span><span class="sxs-lookup"><span data-stu-id="5a071-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="5a071-107">기본: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="5a071-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="5a071-108">Multi-factor bit Pauli 연산자로 표현 된의 확률을 어설션하는 측정 효과입니다.</span><span class="sxs-lookup"><span data-stu-id="5a071-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5a071-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5a071-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5a071-110">어설션을 만들 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="5a071-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="5a071-111">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="5a071-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="5a071-112">의 예상 결과 `Measure(bases, qubits)` 입니다.</span><span class="sxs-lookup"><span data-stu-id="5a071-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="5a071-113">문제: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a071-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5a071-114">지정 된 결과가 예상 되는 확률입니다.</span><span class="sxs-lookup"><span data-stu-id="5a071-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="5a071-115">msg: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="5a071-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="5a071-116">어설션이 실패 하는 경우 보고 될 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="5a071-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="5a071-117">를: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a071-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="5a071-118">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a071-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5a071-119">설명</span><span class="sxs-lookup"><span data-stu-id="5a071-119">Remarks</span></span>

<span data-ttu-id="5a071-120">이 작업의 Adjoint 및 제어 된 버전은 조건을 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a071-120">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a071-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5a071-121">See Also</span></span>

- [<span data-ttu-id="5a071-122">AssertMeasurement.</span><span class="sxs-lookup"><span data-stu-id="5a071-122">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)