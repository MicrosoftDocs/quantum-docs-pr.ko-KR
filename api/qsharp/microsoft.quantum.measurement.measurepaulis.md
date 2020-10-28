---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: MeasurePaulis 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 7348ab3941af391c451d5c66f888cf3b6662cf20
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720344"
---
# <a name="measurepaulis-operation"></a><span data-ttu-id="d0e35-102">MeasurePaulis 작업</span><span class="sxs-lookup"><span data-stu-id="d0e35-102">MeasurePaulis operation</span></span>

<span data-ttu-id="d0e35-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="d0e35-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="d0e35-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0e35-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0e35-105">여러 가지 기능을 제공 하는 배열에서 지정 된 측정 가젯을 사용 하 여 각 측정값을 측정 한 다음 결과의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0e35-105">Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.</span></span>

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a><span data-ttu-id="d0e35-106">입력</span><span class="sxs-lookup"><span data-stu-id="d0e35-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="d0e35-107">paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="d0e35-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="d0e35-108">측정할 다중값 비트 Pauli 연산자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d0e35-108">Array of multi-qubit Pauli operators to measure.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d0e35-109">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d0e35-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d0e35-110">지정 된 연산자를 측정할 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="d0e35-110">Register on which to measure the given operators.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="d0e35-111">가젯: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => __잘못 되었습니다 <Result>__ .</span><span class="sxs-lookup"><span data-stu-id="d0e35-111">gadget : ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="d0e35-112">지정 된 여러 기능 비트 연산자의 측정을 수행 하는 연산입니다.</span><span class="sxs-lookup"><span data-stu-id="d0e35-112">Operation which performs the measurement of a given multi-qubit operator.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d0e35-113">출력: __잘못 <Result> 된__ []</span><span class="sxs-lookup"><span data-stu-id="d0e35-113">Output : __invalid<Result>__ []</span></span>

<span data-ttu-id="d0e35-114">의 각 요소를 측정 하 여 가져온 결과의 `paulis` 배열 `target` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d0e35-114">The array of results obtained from measuring each element of `paulis` on `target`.</span></span>