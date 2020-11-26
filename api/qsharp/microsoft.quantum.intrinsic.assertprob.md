---
uid: Microsoft.Quantum.Intrinsic.AssertProb
title: AssertProb 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: AssertProb
qsharp.summary: >-
  > [!WARNING]

  > AssertProb has been deprecated. Please use <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> instead.
ms.openlocfilehash: 3c0f7c7a9e0190c5a8e5f3e70a5f82a8c23a97bc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199100"
---
# <a name="assertprob-operation"></a><span data-ttu-id="cd670-102">AssertProb 작업</span><span class="sxs-lookup"><span data-stu-id="cd670-102">AssertProb operation</span></span>

<span data-ttu-id="cd670-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="cd670-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="cd670-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="cd670-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


> [!WARNING]
> <span data-ttu-id="cd670-105">AssertProb는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd670-105">AssertProb has been deprecated.</span></span> <span data-ttu-id="cd670-106">대신 <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd670-106">Please use <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> instead.</span></span>



```qsharp
operation AssertProb (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cd670-107">입력</span><span class="sxs-lookup"><span data-stu-id="cd670-107">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="cd670-108">기본: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="cd670-108">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>




### <a name="qubits--qubit"></a><span data-ttu-id="cd670-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cd670-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="result--__invalidresult__"></a><span data-ttu-id="cd670-110">결과: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="cd670-110">result : __invalid<Result>__</span></span>




### <a name="prob--double"></a><span data-ttu-id="cd670-111">문제: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cd670-111">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="msg--string"></a><span data-ttu-id="cd670-112">msg: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="cd670-112">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>




### <a name="tol--double"></a><span data-ttu-id="cd670-113">를: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cd670-113">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="cd670-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cd670-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

