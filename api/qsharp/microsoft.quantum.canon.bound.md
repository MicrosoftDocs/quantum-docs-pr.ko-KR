---
uid: Microsoft.Quantum.Canon.Bound
title: Bound 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Bound
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.
ms.openlocfilehash: 34ca2b79d0ee09bd3b5b5b3f0c0b20420d5b3882
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716703"
---
# <a name="bound-function"></a><span data-ttu-id="144ae-102">Bound 함수</span><span class="sxs-lookup"><span data-stu-id="144ae-102">Bound function</span></span>

<span data-ttu-id="144ae-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="144ae-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="144ae-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="144ae-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="144ae-105">단일 입력에 대해 작동 하는 작업 배열이 지정 된 경우 지정 된 각 작업을 순서 대로 수행 하는 새 작업을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="144ae-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>

```qsharp
function Bound<'T> (operations : ('T => Unit)[]) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="144ae-106">입력</span><span class="sxs-lookup"><span data-stu-id="144ae-106">Input</span></span>

### <a name="operations--t--unit-"></a><span data-ttu-id="144ae-107">작업: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="144ae-107">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="144ae-108">지정 된 입력에 대해 수행할 일련의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="144ae-108">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="144ae-109">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="144ae-109">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="144ae-110">지정 된 각 작업을 입력에 대해 순서 대로 수행 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="144ae-110">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="144ae-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="144ae-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="144ae-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="144ae-112">'T</span></span>

<span data-ttu-id="144ae-113">배열의 각 작업이 작동 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="144ae-113">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="144ae-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="144ae-114">See Also</span></span>

- [<span data-ttu-id="144ae-115">BoundC입니다.</span><span class="sxs-lookup"><span data-stu-id="144ae-115">Microsoft.Quantum.Canon.BoundC</span></span>](xref:Microsoft.Quantum.Canon.BoundC)
- [<span data-ttu-id="144ae-116">BoundA입니다.</span><span class="sxs-lookup"><span data-stu-id="144ae-116">Microsoft.Quantum.Canon.BoundA</span></span>](xref:Microsoft.Quantum.Canon.BoundA)
- [<span data-ttu-id="144ae-117">BoundCA입니다.</span><span class="sxs-lookup"><span data-stu-id="144ae-117">Microsoft.Quantum.Canon.BoundCA</span></span>](xref:Microsoft.Quantum.Canon.BoundCA)