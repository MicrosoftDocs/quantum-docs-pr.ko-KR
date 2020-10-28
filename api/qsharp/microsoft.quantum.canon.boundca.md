---
uid: Microsoft.Quantum.Canon.BoundCA
title: BoundCA 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: d96d33781def10940479ba2eafdcc6711a0c05a5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716633"
---
# <a name="boundca-function"></a><span data-ttu-id="6e796-102">BoundCA 함수</span><span class="sxs-lookup"><span data-stu-id="6e796-102">BoundCA function</span></span>

<span data-ttu-id="6e796-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6e796-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6e796-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6e796-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6e796-105">단일 입력에 대해 작동 하는 작업 배열이 지정 된 경우 지정 된 각 작업을 순서 대로 수행 하는 새 작업을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e796-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="6e796-106">한정자는 `CA` 배열의 모든 작업이 adjointable 및 제어 가능 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e796-106">The modifier `CA` indicates that all operations in the array are adjointable and controllable.</span></span>

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="6e796-107">입력</span><span class="sxs-lookup"><span data-stu-id="6e796-107">Input</span></span>

### <a name="operations--t--unit-adj--ctl"></a><span data-ttu-id="6e796-108">작업: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl []</span><span class="sxs-lookup"><span data-stu-id="6e796-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="6e796-109">지정 된 입력에 대해 수행할 일련의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="6e796-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit-adj--ctl"></a><span data-ttu-id="6e796-110">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="6e796-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="6e796-111">지정 된 각 작업을 입력에 대해 순서 대로 수행 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="6e796-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6e796-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6e796-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6e796-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="6e796-113">'T</span></span>

<span data-ttu-id="6e796-114">배열의 각 작업이 작동 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="6e796-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e796-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6e796-115">See Also</span></span>

- [<span data-ttu-id="6e796-116">Microsoft. 양자.</span><span class="sxs-lookup"><span data-stu-id="6e796-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)