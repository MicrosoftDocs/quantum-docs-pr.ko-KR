---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: WithZeroInsertedAt 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228868"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="17804-102">WithZeroInsertedAt 함수</span><span class="sxs-lookup"><span data-stu-id="17804-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="17804-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="17804-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="17804-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="17804-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="17804-105">0 비트를 정수에 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="17804-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="17804-106">Description</span><span class="sxs-lookup"><span data-stu-id="17804-106">Description</span></span>

<span data-ttu-id="17804-107">이 작업은 정수를 사용 하 고 0을 비트 `position` 단위로 삽입 한 다음 업데이트 된 값을 정수로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="17804-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="17804-108">예를 들어 10 ($10 _ = 1010_ $)의 위치 2에 0을 삽입 하면 {10} {2} 숫자 18 ($18 _ {10} = 10010_ {2} $)이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17804-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="17804-109">입력</span><span class="sxs-lookup"><span data-stu-id="17804-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="17804-110">position: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="17804-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="17804-111">0이 삽입 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="17804-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="17804-112">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="17804-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="17804-113">수정 된 값</span><span class="sxs-lookup"><span data-stu-id="17804-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="17804-114">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="17804-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="17804-115">수정 된 값</span><span class="sxs-lookup"><span data-stu-id="17804-115">Modified value</span></span>