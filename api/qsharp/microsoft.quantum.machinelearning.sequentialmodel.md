---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: SequentialModel 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: ab9c121884e489b5d056285008c91c1ad70bb053
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854890"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="c4060-102">SequentialModel 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="c4060-102">SequentialModel user defined type</span></span>

<span data-ttu-id="c4060-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c4060-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="c4060-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c4060-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="c4060-105">매개 변수화 되 고 제어 되는 회전, 회전 각도 할당 및 모델에서 인식 되는 두 클래스 간의 바이어스로 구성 된 퀀텀 분류자 모델에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4060-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="c4060-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="c4060-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="c4060-107">구조: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="c4060-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="c4060-108">입력을 분류 하는 데 사용 되는 제어 되는 회전의 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="c4060-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="c4060-109">매개 변수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c4060-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c4060-110">지정 된 분류 구조에 대 한 회전 각도를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4060-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="c4060-111">바이어스: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c4060-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c4060-112">이 분류자가 인식 하는 두 클래스 간의 편차입니다.</span><span class="sxs-lookup"><span data-stu-id="c4060-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="c4060-113">참조</span><span class="sxs-lookup"><span data-stu-id="c4060-113">References</span></span>

- [<span data-ttu-id="c4060-114">arXiv: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="c4060-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)