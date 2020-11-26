---
uid: Microsoft.Quantum.Convert.Call
title: 작업 호출
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 92c159cef878fb587b0ed514fd6660dd19527cab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214214"
---
# <a name="call-operation"></a><span data-ttu-id="945b0-102">작업 호출</span><span class="sxs-lookup"><span data-stu-id="945b0-102">Call operation</span></span>

<span data-ttu-id="945b0-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="945b0-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="945b0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="945b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="945b0-105">지정 된 입력을 사용 하 여 함수를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="945b0-105">Calls a function with a given input.</span></span>

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a><span data-ttu-id="945b0-106">Description</span><span class="sxs-lookup"><span data-stu-id="945b0-106">Description</span></span>

<span data-ttu-id="945b0-107">함수 및이 함수에 대 한 입력이 지정 되 면는 함수를 호출 하 고 해당 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="945b0-107">Given a function and an input to that function, calls the function and returns its output.</span></span>

## <a name="input"></a><span data-ttu-id="945b0-108">입력</span><span class="sxs-lookup"><span data-stu-id="945b0-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="945b0-109">fn: ' 입력 > ' 출력</span><span class="sxs-lookup"><span data-stu-id="945b0-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="945b0-110">호출할 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="945b0-110">A function to be called.</span></span>


### <a name="input--input"></a><span data-ttu-id="945b0-111">입력: ' 입력</span><span class="sxs-lookup"><span data-stu-id="945b0-111">input : 'Input</span></span>

<span data-ttu-id="945b0-112">함수에 전달 되는 입력입니다.</span><span class="sxs-lookup"><span data-stu-id="945b0-112">The input to be passed to the function.</span></span>



## <a name="output--output"></a><span data-ttu-id="945b0-113">출력: ' 출력</span><span class="sxs-lookup"><span data-stu-id="945b0-113">Output : 'Output</span></span>

<span data-ttu-id="945b0-114">호출하는 `fn`의 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="945b0-114">The result of calling `fn`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="945b0-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="945b0-115">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="945b0-116">' 입력</span><span class="sxs-lookup"><span data-stu-id="945b0-116">'Input</span></span>


### <a name="output"></a><span data-ttu-id="945b0-117">' 출력</span><span class="sxs-lookup"><span data-stu-id="945b0-117">'Output</span></span>



## <a name="remarks"></a><span data-ttu-id="945b0-118">설명</span><span class="sxs-lookup"><span data-stu-id="945b0-118">Remarks</span></span>

<span data-ttu-id="945b0-119">이 작업은 작업 내의 특정 위치에서 함수를 강제로 호출 하거나 작업이 필요한 함수를 호출 하는 데 주로 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="945b0-119">This operation is mainly useful for forcing a function to be called at a specific place within an operation, or for calling a function where an operation is expected.</span></span>