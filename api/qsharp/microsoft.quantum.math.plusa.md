---
uid: Microsoft.Quantum.Math.PlusA
title: PlusA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PlusA
qsharp.summary: Returns the sum (concatenation) of two inputs.
ms.openlocfilehash: 0c6fdcf7c59dc5d89bf83e285339046b5ad5a57e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709605"
---
# <a name="plusa-function"></a><span data-ttu-id="7f9c0-102">PlusA 함수</span><span class="sxs-lookup"><span data-stu-id="7f9c0-102">PlusA function</span></span>

<span data-ttu-id="7f9c0-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="7f9c0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="7f9c0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7f9c0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7f9c0-105">두 입력의 합 (연결)을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f9c0-105">Returns the sum (concatenation) of two inputs.</span></span>

```qsharp
function PlusA<'Element> (a : 'Element[], b : 'Element[]) : 'Element[]
```


## <a name="input"></a><span data-ttu-id="7f9c0-106">입력</span><span class="sxs-lookup"><span data-stu-id="7f9c0-106">Input</span></span>

### <a name="a--element"></a><span data-ttu-id="7f9c0-107">a: ' 요소 []</span><span class="sxs-lookup"><span data-stu-id="7f9c0-107">a : 'Element[]</span></span>

<span data-ttu-id="7f9c0-108">합계를 구할 첫 번째 입력 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="7f9c0-108">The first input $a$ to be summed.</span></span>


### <a name="b--element"></a><span data-ttu-id="7f9c0-109">b: ' 요소 []</span><span class="sxs-lookup"><span data-stu-id="7f9c0-109">b : 'Element[]</span></span>

<span data-ttu-id="7f9c0-110">합계를 구할 두 번째 입력 $b $입니다.</span><span class="sxs-lookup"><span data-stu-id="7f9c0-110">The second input $b$ to be summed.</span></span>



## <a name="output--element"></a><span data-ttu-id="7f9c0-111">Output: ' 요소 []</span><span class="sxs-lookup"><span data-stu-id="7f9c0-111">Output : 'Element[]</span></span>

<span data-ttu-id="7f9c0-112">Sum $a + b $입니다.</span><span class="sxs-lookup"><span data-stu-id="7f9c0-112">The sum $a + b$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7f9c0-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f9c0-113">Type Parameters</span></span>

### <a name="element"></a><span data-ttu-id="7f9c0-114">' 요소</span><span class="sxs-lookup"><span data-stu-id="7f9c0-114">'Element</span></span>

<span data-ttu-id="7f9c0-115">두 입력 배열의 각 요소에 대 한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7f9c0-115">The type of each element in each of the two input arrays.</span></span>