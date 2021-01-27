---
uid: Microsoft.Quantum.Canon.BoundC
title: BoundC 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 6b640c0dab14778336f42098e699e7e68cc726df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841039"
---
# <a name="boundc-function"></a><span data-ttu-id="fa9bd-102">BoundC 함수</span><span class="sxs-lookup"><span data-stu-id="fa9bd-102">BoundC function</span></span>

<span data-ttu-id="fa9bd-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fa9bd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fa9bd-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fa9bd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fa9bd-105">단일 입력에 대해 작동 하는 작업 배열이 지정 된 경우 지정 된 각 작업을 순서 대로 수행 하는 새 작업을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="fa9bd-106">한정자는 `C` 배열의 모든 작업이 제어 가능 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="fa9bd-107">입력</span><span class="sxs-lookup"><span data-stu-id="fa9bd-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="fa9bd-108">작업: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl []입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="fa9bd-109">지정 된 입력에 대해 수행할 일련의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="fa9bd-110">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="fa9bd-111">지정 된 각 작업을 입력에 대해 순서 대로 수행 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fa9bd-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa9bd-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fa9bd-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="fa9bd-113">'T</span></span>

<span data-ttu-id="fa9bd-114">배열의 각 작업이 작동 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-114">The target on which each of the operations in the array act.</span></span>

## <a name="example"></a><span data-ttu-id="fa9bd-115">예</span><span class="sxs-lookup"><span data-stu-id="fa9bd-115">Example</span></span>

<span data-ttu-id="fa9bd-116">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-116">The following are equivalent:</span></span>

```qsharp
let bound = BoundC([U, V]);
bound(x);
```

<span data-ttu-id="fa9bd-117">및</span><span class="sxs-lookup"><span data-stu-id="fa9bd-117">and</span></span>

```qsharp
U(x); V(x);
```

## <a name="see-also"></a><span data-ttu-id="fa9bd-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fa9bd-118">See Also</span></span>

- [<span data-ttu-id="fa9bd-119">Microsoft. 양자.</span><span class="sxs-lookup"><span data-stu-id="fa9bd-119">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)