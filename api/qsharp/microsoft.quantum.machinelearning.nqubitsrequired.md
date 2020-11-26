---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: NQubitsRequired 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: e910edb9bf432e6acb5c349ee6b9d65797aaaba7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211664"
---
# <a name="nqubitsrequired-function"></a><span data-ttu-id="69620-102">NQubitsRequired 함수</span><span class="sxs-lookup"><span data-stu-id="69620-102">NQubitsRequired function</span></span>

<span data-ttu-id="69620-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="69620-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="69620-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="69620-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="69620-105">지정 된 순차 분류자를 적용 하는 데 필요한 원하는 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69620-105">Returns the number of qubits required to apply a given sequential classifier.</span></span>

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a><span data-ttu-id="69620-106">입력</span><span class="sxs-lookup"><span data-stu-id="69620-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="69620-107">모델: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="69620-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--int"></a><span data-ttu-id="69620-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="69620-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="69620-109">순차 분류자가 적용 될 수 있는 레지스터의 최소 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="69620-109">The minimum size of a register on which the sequential classifier may be applied.</span></span>