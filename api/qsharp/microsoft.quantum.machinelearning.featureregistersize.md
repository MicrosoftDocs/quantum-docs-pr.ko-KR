---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: FeatureRegisterSize 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 2754e901d74175c1841a38d795f5de02dabc9b8d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848437"
---
# <a name="featureregistersize-function"></a><span data-ttu-id="9012c-102">FeatureRegisterSize 함수</span><span class="sxs-lookup"><span data-stu-id="9012c-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="9012c-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9012c-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="9012c-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9012c-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="9012c-105">특정 기능 벡터를 인코딩하는 데 필요한 원하는 비트 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9012c-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="9012c-106">입력</span><span class="sxs-lookup"><span data-stu-id="9012c-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="9012c-107">샘플: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9012c-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9012c-108">요소 비트 레지스터로 인코딩할 샘플 기능 벡터입니다.</span><span class="sxs-lookup"><span data-stu-id="9012c-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="9012c-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9012c-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9012c-110">원하는 `sample` 비트 수로 표현 되는 원하는 비트 레지스터로 인코딩하는 데 필요한 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="9012c-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>