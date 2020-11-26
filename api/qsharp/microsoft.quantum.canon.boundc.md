---
uid: Microsoft.Quantum.Canon.BoundC
title: BoundC 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 02e9b6a9676cdd1996d3a2413b2a6383e3a4e90e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207584"
---
# <a name="boundc-function"></a><span data-ttu-id="0b039-102">BoundC 함수</span><span class="sxs-lookup"><span data-stu-id="0b039-102">BoundC function</span></span>

<span data-ttu-id="0b039-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0b039-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0b039-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0b039-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0b039-105">단일 입력에 대해 작동 하는 작업 배열이 지정 된 경우 지정 된 각 작업을 순서 대로 수행 하는 새 작업을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b039-105">Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence.</span></span>
<span data-ttu-id="0b039-106">한정자는 `C` 배열의 모든 작업이 제어 가능 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0b039-106">The modifier `C` indicates that all operations in the array are controllable.</span></span>

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="0b039-107">입력</span><span class="sxs-lookup"><span data-stu-id="0b039-107">Input</span></span>

### <a name="operations--t--unit--is-ctl"></a><span data-ttu-id="0b039-108">작업: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl []입니다.</span><span class="sxs-lookup"><span data-stu-id="0b039-108">operations : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="0b039-109">지정 된 입력에 대해 수행할 일련의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0b039-109">A sequence of operations to be performed on a given input.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="0b039-110">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="0b039-110">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="0b039-111">지정 된 각 작업을 입력에 대해 순서 대로 수행 하는 새 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0b039-111">A new operation that performs each given operation in sequence on its input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0b039-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0b039-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0b039-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="0b039-113">'T</span></span>

<span data-ttu-id="0b039-114">배열의 각 작업이 작동 하는 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="0b039-114">The target on which each of the operations in the array act.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b039-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0b039-115">See Also</span></span>

- [<span data-ttu-id="0b039-116">Microsoft. 양자.</span><span class="sxs-lookup"><span data-stu-id="0b039-116">Microsoft.Quantum.Canon.Bound</span></span>](xref:Microsoft.Quantum.Canon.Bound)