---
title: 클래식 데이터 로드
description: 사용자 고유의 데이터 집합을 로드 하 여 Microsoft Quantum Development Kit (QDK)로 분류자 모델을 학습 하는 방법을 알아봅니다.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.load
ms.openlocfilehash: 15e63ced6223759a332ce22a43c133a7899f482a
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909962"
---
# <a name="load-and-classify-your-own-datasets"></a><span data-ttu-id="22011-103">사용자 고유의 데이터 집합 로드 및 분류</span><span class="sxs-lookup"><span data-stu-id="22011-103">Load and classify your own datasets</span></span>

<span data-ttu-id="22011-104">이 간단한 자습서에서는 사용자 고유의 데이터 집합을 로드 하 여 QDK (퀀텀 개발 키트)로 분류자 모델을 학습 하는 방법에 대해 알아보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-104">In this short tutorial, we are going to learn how to load your own dataset to train a classifier model with the Quantum Development Kit (QDK).</span></span>

<span data-ttu-id="22011-105">[JSON 파일](https://en.wikipedia.org/wiki/JSON) 등의 표준화 된 serialization 형식을 사용 하 여 데이터를 저장 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-105">We highly recommend the use of a standardized serialization format such as [JSON files](https://en.wikipedia.org/wiki/JSON) to store your data.</span></span>
<span data-ttu-id="22011-106">이러한 형식은 Python 및 .NET 에코 시스템과 같은 다른 프레임 워크와의 높은 호환성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-106">Such formats offer high compatibility with different frameworks like Python and the .NET ecosystem.</span></span>
<span data-ttu-id="22011-107">특히 샘플에서 직접 코드를 복사 하 여 붙여넣을 수 있도록 데이터를 로드 하는 데 템플릿을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-107">In particular, we recommend using our template for loading the data, so that you can copy-paste the code directly from the samples.</span></span>

## <a name="template-for-loading-your-datasets"></a><span data-ttu-id="22011-108">데이터 집합을 로드 하기 위한 템플릿</span><span class="sxs-lookup"><span data-stu-id="22011-108">Template for loading your datasets</span></span>

<span data-ttu-id="22011-109">크기 $N = $2의 학습 데이터 집합 $ (x, y) $가 있다고 가정해 보겠습니다. $x $의 _i $ $x 각 인스턴스에는 $x _ {i1} $, $x _ {i2} $ 및 $x _ {i3} $와 같은 세 가지 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-109">Suppose we have a training dataset $(x, y)$ of size $N=2$ where each instance $x_i$ of $x$ has three features: $x_{i1}$, $x_{i2}$ and $x_{i3}$.</span></span>
<span data-ttu-id="22011-110">유효성 검사 데이터 집합의 구조가 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-110">The validation dataset has the same structure.</span></span>
<span data-ttu-id="22011-111">이러한 datsets는 다음과 유사한 `data.json` 파일로 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-111">These datsets can be represented by a `data.json` file similar to the following:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                x_11,
                x_12,
                x_13
            ],
            [
                x_21,
                x_22,
                x_23
            ]
        ],
        "Labels": [
            y_1,
            y_2
        ]
    },
    "ValidationData": {
        "Features": [
            [
                xv_11,
                xv_12,
                xv_13
            ],
            [
                xv_11,
                xv_12,
                xv_13
            ]
        ],
        "Labels": [
            yv_1,
            yv_2
        ]
    }
}
```

### <a name="example-using-the-template"></a><span data-ttu-id="22011-112">템플릿 사용 예</span><span class="sxs-lookup"><span data-stu-id="22011-112">Example using the template</span></span>

<span data-ttu-id="22011-113">다른 고양이와 강아지의 높이와 가중치가 있는 작은 데이터 집합이 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-113">Suppose we have a small dataset with the heights and weights of different cats and dogs.</span></span> <span data-ttu-id="22011-114">이 데이터 집합은 모델을 학습 하는 데 매우 작지만 데이터 집합 로드 프로세스를 표시 하는 데에는 충분 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-114">This dataset is very small to train a model but will be enough to show the process of loading a dataset.</span></span>

| <span data-ttu-id="22011-115">높이 (m)</span><span class="sxs-lookup"><span data-stu-id="22011-115">Height (m)</span></span> | <span data-ttu-id="22011-116">무게 (kg)</span><span class="sxs-lookup"><span data-stu-id="22011-116">Weight (kg)</span></span> | <span data-ttu-id="22011-117">동물</span><span class="sxs-lookup"><span data-stu-id="22011-117">Animal</span></span> |
|-----------|------------|--------|
| <span data-ttu-id="22011-118">0.54</span><span class="sxs-lookup"><span data-stu-id="22011-118">0.54</span></span>      | <span data-ttu-id="22011-119">30</span><span class="sxs-lookup"><span data-stu-id="22011-119">30</span></span>         | <span data-ttu-id="22011-120">Dog</span><span class="sxs-lookup"><span data-stu-id="22011-120">Dog</span></span>    |
| <span data-ttu-id="22011-121">0.30</span><span class="sxs-lookup"><span data-stu-id="22011-121">0.30</span></span>      | <span data-ttu-id="22011-122">8</span><span class="sxs-lookup"><span data-stu-id="22011-122">8</span></span>          | <span data-ttu-id="22011-123">Cat</span><span class="sxs-lookup"><span data-stu-id="22011-123">Cat</span></span>    |
| <span data-ttu-id="22011-124">0.91</span><span class="sxs-lookup"><span data-stu-id="22011-124">0.91</span></span>      | <span data-ttu-id="22011-125">44</span><span class="sxs-lookup"><span data-stu-id="22011-125">44</span></span>         | <span data-ttu-id="22011-126">Dog</span><span class="sxs-lookup"><span data-stu-id="22011-126">Dog</span></span>    |
| <span data-ttu-id="22011-127">0.86</span><span class="sxs-lookup"><span data-stu-id="22011-127">0.86</span></span>      | <span data-ttu-id="22011-128">31</span><span class="sxs-lookup"><span data-stu-id="22011-128">31</span></span>          | <span data-ttu-id="22011-129">Dog</span><span class="sxs-lookup"><span data-stu-id="22011-129">Dog</span></span>    |
| <span data-ttu-id="22011-130">0.32</span><span class="sxs-lookup"><span data-stu-id="22011-130">0.32</span></span>      | <span data-ttu-id="22011-131">5</span><span class="sxs-lookup"><span data-stu-id="22011-131">5</span></span>         | <span data-ttu-id="22011-132">Cat</span><span class="sxs-lookup"><span data-stu-id="22011-132">Cat</span></span>    |
| <span data-ttu-id="22011-133">0.25</span><span class="sxs-lookup"><span data-stu-id="22011-133">0.25</span></span>      | <span data-ttu-id="22011-134">4</span><span class="sxs-lookup"><span data-stu-id="22011-134">4</span></span>          | <span data-ttu-id="22011-135">Cat</span><span class="sxs-lookup"><span data-stu-id="22011-135">Cat</span></span>    |

<span data-ttu-id="22011-136">프로세스는.</span><span class="sxs-lookup"><span data-stu-id="22011-136">The process is:</span></span>

- <span data-ttu-id="22011-137">먼저 데이터 집합을 학습 및 유효성 검사로 구분 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-137">First we need to separate the dataset into training and validation.</span></span> <span data-ttu-id="22011-138">이 경우 학습을 위한 처음 3 개의 샘플 및 유효성 검사를 위한 샘플의 나머지 부분을 수행 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22011-138">In this case we can just take the first three samples for training and the rest of samples for validation.</span></span> <span data-ttu-id="22011-139">일반적으로 학습 데이터에 원치 않는 편향을 방지 하기 위해 무작위로 학습 및 유효성 검사 데이터 집합을 샘플링 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-139">In general it is a good practice to sample randomly the training and validation dataset to avoid unwanted biases in the training data.</span></span>
- <span data-ttu-id="22011-140">두 번째로, 각 클래스에 숫자 레이블을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-140">Secondly, we need to assign a numeric label to each class.</span></span> <span data-ttu-id="22011-141">지금은 QML 라이브러리는 이진 분류 문제만 인정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-141">Note that, for the moment, the QML library only admits binary classification problems.</span></span> <span data-ttu-id="22011-142">따라서 클래스 `Dog`에 레이블 0을 할당 하 고 클래스 `Cat`에 숫자 1을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-142">So we will assign the label 0 to the class `Dog` and the number 1 to the class `Cat`.</span></span>
- <span data-ttu-id="22011-143">마지막으로, 데이터 집합의 데이터를 사용 하 여 템플릿을 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="22011-143">Finally, we fill the template using the data from our dataset.</span></span> <span data-ttu-id="22011-144">빅 데이터 집합의 경우 특정 데이터 집합에서 템플릿을 자동으로 생성 하는 작은 스크립트를 작성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-144">Note that for big datasets you should build a small script to automatically generate the template from your specific dataset.</span></span> <span data-ttu-id="22011-145">이 스크립트는 데이터 집합의 원본 형식에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="22011-145">This script will depend on the original format of your dataset.</span></span>

<span data-ttu-id="22011-146">데이터 집합의 경우 `data.json` 파일은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-146">For our dataset the `data.json` file is:</span></span>

```json
{
    "TrainingData": {
        "Features": [
            [
                0.54,
                30
            ],
            [
                0.30,
                8
            ],
            [
                0.91,
                44
            ]
        ],
        "Labels": [
            0,
            1,
            0
        ]
    },
    "ValidationData": {
        "Features": [
            [
                0.86,
                31
            ],
            [
                0.32,
                5
            ]
            [
                0.25,
                4
            ]
        ],
        "Labels": [
            0,
            1,
            1
        ]
    }
}

```

## <a name="loading-the-data"></a><span data-ttu-id="22011-147">데이터 로드</span><span class="sxs-lookup"><span data-stu-id="22011-147">Loading the data</span></span>

<span data-ttu-id="22011-148">JSON 파일로 serialize 된 데이터를 사용 하는 경우 선택한 호스트 언어와 함께 제공 되는 JSON 라이브러리를 사용 하 여 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-148">Once you have your data serialized as a JSON file, you can load it in using JSON libraries provided with your host language of choice.</span></span>

### <a name="python"></a>[<span data-ttu-id="22011-149">Python</span><span class="sxs-lookup"><span data-stu-id="22011-149">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="22011-150">Python은 JSON 직렬화 된 데이터로 작업 하기 위한 [기본 제공 `json` 패키지](https://docs.python.org/3.7/library/json.html) 를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-150">Python provides the [built-in `json` package](https://docs.python.org/3.7/library/json.html) for working with JSON-serialized data:</span></span>

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[<span data-ttu-id="22011-151">C#</span><span class="sxs-lookup"><span data-stu-id="22011-151">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="22011-152">.NET Core 플랫폼은 JSON 직렬화 된 데이터로 작업 하기 위한 [`System.Text.Json` 패키지](https://www.nuget.org/packages/System.Text.Json) 를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="22011-152">The .NET Core platform provides the [`System.Text.Json` package](https://www.nuget.org/packages/System.Text.Json) for working with JSON-serialized data:</span></span>

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="whats-next"></a><span data-ttu-id="22011-153">다음 단계</span><span class="sxs-lookup"><span data-stu-id="22011-153">What's next?</span></span>

<span data-ttu-id="22011-154">이제 고유한 데이터 집합을 사용 하 여 사용자 고유의 실험을 실행할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="22011-154">Now you are ready to start running your own experiments with your own datasets.</span></span> <span data-ttu-id="22011-155">다른 분류자와 데이터 집합을 시도 하 고 결과를 공유 하는 커뮤니티에 기여 하세요.</span><span class="sxs-lookup"><span data-stu-id="22011-155">Try different classifiers and dataset and contribute to the community sharing your results!</span></span>
