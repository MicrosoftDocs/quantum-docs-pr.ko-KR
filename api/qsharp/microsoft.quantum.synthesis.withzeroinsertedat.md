---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: WithZeroInsertedAt 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 6e13251741dadb19740b208cdfc13a14964a48dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725156"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="1cc12-102">WithZeroInsertedAt 함수</span><span class="sxs-lookup"><span data-stu-id="1cc12-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="1cc12-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="1cc12-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="1cc12-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1cc12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1cc12-105">0 비트를 정수에 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cc12-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="1cc12-106">Description</span><span class="sxs-lookup"><span data-stu-id="1cc12-106">Description</span></span>

<span data-ttu-id="1cc12-107">이 작업은 정수를 사용 하 고 0을 비트 `position` 단위로 삽입 한 다음 업데이트 된 값을 정수로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cc12-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="1cc12-108">예를 들어 10 ($10 _ = 1010_ $)의 위치 2에 0을 삽입 하면 {10} {2} 숫자 18 ($18 _ {10} = 10010_ {2} $)이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cc12-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="1cc12-109">입력</span><span class="sxs-lookup"><span data-stu-id="1cc12-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="1cc12-110">position: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cc12-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1cc12-111">0이 삽입 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1cc12-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="1cc12-112">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cc12-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1cc12-113">수정 된 값</span><span class="sxs-lookup"><span data-stu-id="1cc12-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="1cc12-114">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cc12-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1cc12-115">수정 된 값</span><span class="sxs-lookup"><span data-stu-id="1cc12-115">Modified value</span></span>