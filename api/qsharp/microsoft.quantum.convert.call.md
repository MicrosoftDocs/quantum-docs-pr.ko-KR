---
uid: Microsoft.Quantum.Convert.Call
title: 작업 호출
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850203"
---
# <a name="call-operation"></a><span data-ttu-id="b51da-102">작업 호출</span><span class="sxs-lookup"><span data-stu-id="b51da-102">Call operation</span></span>

<span data-ttu-id="b51da-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="b51da-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="b51da-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b51da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b51da-105">지정 된 입력을 사용 하 여 함수를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="b51da-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="b51da-106">설명</span><span class="sxs-lookup"><span data-stu-id="b51da-106">Description</span></span>

<span data-ttu-id="b51da-107">함수 및이 함수에 대 한 입력이 지정 되 면는 함수를 호출 하 고 해당 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b51da-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="b51da-108">입력</span><span class="sxs-lookup"><span data-stu-id="b51da-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="b51da-109">fn: ' 입력 > ' 출력</span><span class="sxs-lookup"><span data-stu-id="b51da-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="b51da-110">호출할 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="b51da-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="b51da-111">입력: ' 입력</span><span class="sxs-lookup"><span data-stu-id="b51da-111">input : 'Input</span></span>

<span data-ttu-id="b51da-112">함수에 전달 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="b51da-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="b51da-113">출력: ' 출력</span><span class="sxs-lookup"><span data-stu-id="b51da-113">Output : 'Output</span></span>

<span data-ttu-id="b51da-114">호출하는 `fn`의 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="b51da-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b51da-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b51da-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="b51da-116">' 입력</span><span class="sxs-lookup"><span data-stu-id="b51da-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="b51da-117">' 출력</span><span class="sxs-lookup"><span data-stu-id="b51da-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="b51da-118">설명</span><span class="sxs-lookup"><span data-stu-id="b51da-118">Remarks</span></span>

<span data-ttu-id="b51da-119">이 작업은 작업 내의 특정 위치에서 함수를 강제로 호출 하거나 작업이 필요한 함수를 호출 하는 데 주로 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b51da-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>