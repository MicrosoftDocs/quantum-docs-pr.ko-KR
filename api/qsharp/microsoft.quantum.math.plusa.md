---
uid: Microsoft.Quantum.Math.PlusA
title: PlusA 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: fe19c5d2e075624516376a5d5fa49014acb295ec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194834"
---
# <a name="plusa-function"></a><span data-ttu-id="9e9c6-102">PlusA 함수</span><span class="sxs-lookup"><span data-stu-id="9e9c6-102">PlusA function</span></span>

<span data-ttu-id="9e9c6-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9e9c6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9e9c6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e9c6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e9c6-105">두 입력의 합 (연결)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9c6-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="9e9c6-106">입력</span><span class="sxs-lookup"><span data-stu-id="9e9c6-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="9e9c6-107">a: ' 요소 []</span><span class="sxs-lookup"><span data-stu-id="9e9c6-107">a : 'Element[]</span></span>

<span data-ttu-id="9e9c6-108">합계를 구할 첫 번째 입력 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="9e9c6-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="9e9c6-109">b: ' 요소 []</span><span class="sxs-lookup"><span data-stu-id="9e9c6-109">b : 'Element[]</span></span>

<span data-ttu-id="9e9c6-110">합계를 구할 두 번째 입력 $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="9e9c6-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="9e9c6-111">Output: ' 요소 []</span><span class="sxs-lookup"><span data-stu-id="9e9c6-111">Output : 'Element[]</span></span>

<span data-ttu-id="9e9c6-112">Sum $a + b $입니다.</span><span class="sxs-lookup"><span data-stu-id="9e9c6-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9e9c6-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9e9c6-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="9e9c6-114">' 요소</span><span class="sxs-lookup"><span data-stu-id="9e9c6-114">'Element</span></span>

<span data-ttu-id="9e9c6-115">두 입력 배열의 각 요소에 대 한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9e9c6-115">The type of each element in each of the two input arrays.</span></span>