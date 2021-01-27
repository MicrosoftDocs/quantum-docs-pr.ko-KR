---
uid: Microsoft.Quantum.Canon.BoundA
title: BoundA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3d0a5ba5d3d9c76289ed29e59a9c226358b83797
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844536"
---
# <a name="bounda-function"></a><span data-ttu-id="4d802-102">BoundA 함수</span><span class="sxs-lookup"><span data-stu-id="4d802-102">BoundA function</span></span>

<span data-ttu-id="4d802-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4d802-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4d802-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4d802-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4d802-105">단일 입력에 대해 작동 하는 작업 배열이 지정 된 경우 지정 된 각 작업을 순서 대로 수행 하는 새 작업을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d802-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="4d802-106">한정자는 `A` 배열의 모든 작업이 adjointable을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4d802-106">The modifier `A` indicates that all operations in the array are adjointable.</span></span>

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="4d802-107">입력</span><span class="sxs-lookup"><span data-stu-id="4d802-107">Input</span></span>

### <a name="operations--t--unit--is-adj"></a><span data-ttu-id="4d802-108">작업: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj []</span><span class="sxs-lookup"><span data-stu-id="4d802-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="4d802-109">지정 된 입력에 대해 수행할 일련의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4d802-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="4d802-110">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="4d802-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4d802-111">지정 된 각 작업을 입력에 대해 순서 대로 수행 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4d802-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4d802-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d802-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4d802-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="4d802-113">'T</span></span>

<span data-ttu-id="4d802-114">배열의 각 작업이 작동 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="4d802-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="4d802-115">예</span><span class="sxs-lookup"><span data-stu-id="4d802-115">Example</span></span>

<span data-ttu-id="4d802-116">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d802-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundA([U, V]);
bound(x);
```

<span data-ttu-id="4d802-117">및</span><span class="sxs-lookup"><span data-stu-id="4d802-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="4d802-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4d802-118">See Also</span></span>

- [<span data-ttu-id="4d802-119">Microsoft. 양자.</span><span class="sxs-lookup"><span data-stu-id="4d802-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)