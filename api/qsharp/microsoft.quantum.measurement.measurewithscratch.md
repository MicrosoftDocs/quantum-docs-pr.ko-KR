---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: MeasureWithScratch 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: c42316a811e0e4a81c7f244c093a2be88fe5c733
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227066"
---
# <a name="measurewithscratch-operation"></a><span data-ttu-id="60589-102">MeasureWithScratch 작업</span><span class="sxs-lookup"><span data-stu-id="60589-102">MeasureWithScratch operation</span></span>

<span data-ttu-id="60589-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="60589-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="60589-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="60589-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="60589-105">측정을 수행 하기 위해 명시적인 스크래치 비트를 사용 하 여 지정 된 Pauli 연산자를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60589-105">Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.</span></span>

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="60589-106">입력</span><span class="sxs-lookup"><span data-stu-id="60589-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="60589-107">pauli: [pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="60589-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="60589-108">단일 수준 비트 Pauli 연산자의 배열로 지정 된 다중 기능 비트 Pauli 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="60589-108">A multi-qubit Pauli operator specified as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="60589-109">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="60589-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="60589-110">측정할 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="60589-110">Qubit register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="60589-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="60589-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="60589-112">레지스터에서 지정 된 Pauli 연산자를 측정 한 결과입니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="60589-112">The result of measuring the given Pauli operator on the `target` register.</span></span>