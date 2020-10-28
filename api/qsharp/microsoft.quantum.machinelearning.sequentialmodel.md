---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: SequentialModel 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: a425d2155489384ca81ef1c00a5e842bcfb40ae7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722391"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="dc652-102">SequentialModel 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="dc652-102">SequentialModel user defined type</span></span>

<span data-ttu-id="dc652-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dc652-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="dc652-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc652-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc652-105">매개 변수화 되 고 제어 되는 회전, 회전 각도 할당 및 모델에서 인식 되는 두 클래스 간의 바이어스로 구성 된 퀀텀 분류자 모델에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc652-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="dc652-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="dc652-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="dc652-107">구조: [Controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="dc652-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="dc652-108">입력을 분류 하는 데 사용 되는 제어 되는 회전의 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="dc652-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="dc652-109">매개 변수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="dc652-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="dc652-110">지정 된 분류 구조에 대 한 회전 각도를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc652-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="dc652-111">바이어스: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dc652-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dc652-112">이 분류자가 인식 하는 두 클래스 간의 편차입니다.</span><span class="sxs-lookup"><span data-stu-id="dc652-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="dc652-113">참조</span><span class="sxs-lookup"><span data-stu-id="dc652-113">References</span></span>

- [<span data-ttu-id="dc652-114">arXiv: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="dc652-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)