---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: SequentialModel 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: 3afdb8dafe0179535fe5d8c3dff668f1f3de2f7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196177"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="b6ba7-102">SequentialModel 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="b6ba7-102">SequentialModel user defined type</span></span>

<span data-ttu-id="b6ba7-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b6ba7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b6ba7-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b6ba7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="b6ba7-105">매개 변수화 되 고 제어 되는 회전, 회전 각도 할당 및 모델에서 인식 되는 두 클래스 간의 바이어스로 구성 된 퀀텀 분류자 모델에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ba7-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="b6ba7-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="b6ba7-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="b6ba7-107">구조: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="b6ba7-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="b6ba7-108">입력을 분류 하는 데 사용 되는 제어 되는 회전의 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ba7-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="b6ba7-109">매개 변수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b6ba7-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b6ba7-110">지정 된 분류 구조에 대 한 회전 각도를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ba7-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="b6ba7-111">바이어스: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b6ba7-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b6ba7-112">이 분류자가 인식 하는 두 클래스 간의 편차입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ba7-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="b6ba7-113">참조 항목</span><span class="sxs-lookup"><span data-stu-id="b6ba7-113">References</span></span>

- [<span data-ttu-id="b6ba7-114">arXiv: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="b6ba7-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)