---
uid: Microsoft.Quantum.Canon.NoOp
title: NoOp 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 35b6b62cab35f941f04b150dcca763457ddaa084
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205969"
---
# <a name="noop-operation"></a><span data-ttu-id="4e883-102">NoOp 작업</span><span class="sxs-lookup"><span data-stu-id="4e883-102">NoOp operation</span></span>

<span data-ttu-id="4e883-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4e883-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4e883-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4e883-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="4e883-105">인수에 대해 id 연산 (no op)을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-105">Performs the identity operation (no-op) on an argument.</span></span>

```qsharp
operation NoOp<'T> (input : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="4e883-106">Description</span><span class="sxs-lookup"><span data-stu-id="4e883-106">Description</span></span>

<span data-ttu-id="4e883-107">이 작업은 모든 형식의 값을 사용 하 고 아무 것도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-107">This operation takes a value of any type and does nothing to it.</span></span>
<span data-ttu-id="4e883-108">이는 작업 형식의 입력이 예상 될 때마다 유용할 수 있지만 아무 동작도 수행 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-108">This can be useful whenever an input of an operation type is expected, but no action should be taken.</span></span>
<span data-ttu-id="4e883-109">예를 들어 특정 오류 수정 증후군에서 오류가 발생 하지 않았음을 나타내는 경우는 `NoOp<Qubit[]>` 올바른 복구 프로시저일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-109">For instance, if a particular error correction syndrome indicates that no error has occurred, `NoOp<Qubit[]>` may be the correct recovery procedure.</span></span>
<span data-ttu-id="4e883-110">마찬가지로 작업에서 상태 준비 절차를 입력으로 예상 하는 경우에 `NoOp<Qubit[]>` 는 $ \ket{0 \cst0} $ 상태를 준비 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-110">Similarly, if an operation expects a state preparation procedure as input, `NoOp<Qubit[]>` can be used to prepare the state $\ket{0 \cdots 0}$.</span></span>

## <a name="input"></a><span data-ttu-id="4e883-111">입력</span><span class="sxs-lookup"><span data-stu-id="4e883-111">Input</span></span>

### <a name="input--t"></a><span data-ttu-id="4e883-112">입력: ' '</span><span class="sxs-lookup"><span data-stu-id="4e883-112">input : 'T</span></span>

<span data-ttu-id="4e883-113">무시할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-113">A value to be ignored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4e883-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e883-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4e883-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4e883-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4e883-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="4e883-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="4e883-117">설명</span><span class="sxs-lookup"><span data-stu-id="4e883-117">Remarks</span></span>

<span data-ttu-id="4e883-118">거의 모든 경우에 대 한 형식 매개 변수를 `NoOp` 명시적으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-118">In almost all cases, the type parameter for `NoOp` needs to be specified explicitly.</span></span> <span data-ttu-id="4e883-119">예를 들어 `NoOp<Qubit>` 은와 동일 <xref:microsoft.quantum.intrinsic.i> 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e883-119">For instance, `NoOp<Qubit>` is identical to <xref:microsoft.quantum.intrinsic.i>.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e883-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4e883-120">See Also</span></span>

- [<span data-ttu-id="4e883-121">Microsoft 양자</span><span class="sxs-lookup"><span data-stu-id="4e883-121">Microsoft.Quantum.Intrinsic.I</span></span>](xref:Microsoft.Quantum.Intrinsic.I)