---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: FunctionAsOperation 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713511"
---
# <a name="functionasoperation-function"></a><span data-ttu-id="41641-102">FunctionAsOperation 함수</span><span class="sxs-lookup"><span data-stu-id="41641-102">FunctionAsOperation function</span></span>

<span data-ttu-id="41641-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="41641-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="41641-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41641-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41641-105">함수를 작업으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41641-105">Converts functions to operations.</span></span>

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a><span data-ttu-id="41641-106">Description</span><span class="sxs-lookup"><span data-stu-id="41641-106">Description</span></span>

<span data-ttu-id="41641-107">함수가 지정 된 경우 해당 함수를 호출 하 고 다른 작업은 수행 하지 않는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41641-107">Given a function, returns an operation which calls that function, and which does nothing else.</span></span>

## <a name="input"></a><span data-ttu-id="41641-108">입력</span><span class="sxs-lookup"><span data-stu-id="41641-108">Input</span></span>

### <a name="fn--input---output"></a><span data-ttu-id="41641-109">fn: ' 입력 > ' 출력</span><span class="sxs-lookup"><span data-stu-id="41641-109">fn : 'Input -> 'Output</span></span>

<span data-ttu-id="41641-110">작업으로 변환 되는 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="41641-110">A function to be converted to an operation.</span></span>



## <a name="output--input--output"></a><span data-ttu-id="41641-111">출력: ' Input => ' 출력</span><span class="sxs-lookup"><span data-stu-id="41641-111">Output : 'Input => 'Output</span></span> 

<span data-ttu-id="41641-112">`op` `op(input)` 모든에 대해와 동일한 작업입니다 `fn(input)` `input` .</span><span class="sxs-lookup"><span data-stu-id="41641-112">An operation `op` such that `op(input)` is identical to `fn(input)` for all `input`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="41641-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="41641-113">Type Parameters</span></span>

### <a name="input"></a><span data-ttu-id="41641-114">' 입력</span><span class="sxs-lookup"><span data-stu-id="41641-114">'Input</span></span>

<span data-ttu-id="41641-115">변환할 함수의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="41641-115">Input type of the function to be converted.</span></span>
### <a name="output"></a><span data-ttu-id="41641-116">' 출력</span><span class="sxs-lookup"><span data-stu-id="41641-116">'Output</span></span>

<span data-ttu-id="41641-117">변환할 함수의 출력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="41641-117">Output type of the function to be converted.</span></span>

## <a name="remarks"></a><span data-ttu-id="41641-118">설명</span><span class="sxs-lookup"><span data-stu-id="41641-118">Remarks</span></span>

<span data-ttu-id="41641-119">이는 작업을 입력으로 사용할 함수 또는 작업에 함수를 전달 하는 데 주로 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="41641-119">This is mainly useful for passing functions to functions or operations which expect an operation as input.</span></span>