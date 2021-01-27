---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: NQubitsRequired 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: 8f6c1bf3dfef3152a6ba8eada0980d6940724259
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854960"
---
# <a name="nqubitsrequired-function"></a><span data-ttu-id="d48ac-102">NQubitsRequired 함수</span><span class="sxs-lookup"><span data-stu-id="d48ac-102">NQubitsRequired function</span></span>

<span data-ttu-id="d48ac-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d48ac-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d48ac-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d48ac-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d48ac-105">지정 된 순차 분류자를 적용 하는 데 필요한 원하는 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d48ac-105">Returns the number of qubits required to apply a given sequential classifier.</span></span>

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a><span data-ttu-id="d48ac-106">입력</span><span class="sxs-lookup"><span data-stu-id="d48ac-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="d48ac-107">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="d48ac-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--int"></a><span data-ttu-id="d48ac-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d48ac-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d48ac-109">순차 분류자가 적용 될 수 있는 레지스터의 최소 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="d48ac-109">The minimum size of a register on which the sequential classifier may be applied.</span></span>