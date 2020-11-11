---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: AssertMeasurement 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 09024cd8cd6e713360dcf7f42f55941590f35883
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713035"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="2fb6a-102">AssertMeasurement 작업</span><span class="sxs-lookup"><span data-stu-id="2fb6a-102">AssertMeasurement operation</span></span>

<span data-ttu-id="2fb6a-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="2fb6a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="2fb6a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2fb6a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2fb6a-105">지정 된의 지정 된 비트를 측정 하는 어설션은 항상 지정 된 결과를 가집니다.</span><span class="sxs-lookup"><span data-stu-id="2fb6a-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="2fb6a-106">입력</span><span class="sxs-lookup"><span data-stu-id="2fb6a-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="2fb6a-107">기본: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="2fb6a-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="2fb6a-108">Multi-factor bit Pauli 연산자로 표현 된의 확률을 어설션하는 측정 효과입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb6a-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="2fb6a-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2fb6a-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2fb6a-110">어설션을 만들 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb6a-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="2fb6a-111">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="2fb6a-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="2fb6a-112">의 예상 결과 `Measure(bases, qubits)` 입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb6a-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="2fb6a-113">msg: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="2fb6a-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="2fb6a-114">어설션이 실패 하는 경우 보고 될 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb6a-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2fb6a-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2fb6a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2fb6a-116">설명</span><span class="sxs-lookup"><span data-stu-id="2fb6a-116">Remarks</span></span>

<span data-ttu-id="2fb6a-117">이 작업의 Adjoint 및 제어 된 버전은 조건을 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fb6a-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="2fb6a-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2fb6a-118">See Also</span></span>

- [<span data-ttu-id="2fb6a-119">AssertMeasurementProbability.</span><span class="sxs-lookup"><span data-stu-id="2fb6a-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)