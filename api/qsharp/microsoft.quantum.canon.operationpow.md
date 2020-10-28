---
uid: Microsoft.Quantum.Canon.OperationPow
title: OperationPow 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 5cf9017175f44a8a0b8f865624a6c312d25aded1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715772"
---
# <a name="operationpow-function"></a><span data-ttu-id="c0276-102">OperationPow 함수</span><span class="sxs-lookup"><span data-stu-id="c0276-102">OperationPow function</span></span>

<span data-ttu-id="c0276-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c0276-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c0276-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c0276-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c0276-105">전원에 대 한 작업을 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-105">Raises an operation to a power.</span></span>

<span data-ttu-id="c0276-106">즉, $ $U $를 나타내는 작업이 지정 된 경우 power $m $에 대해 ^ m $ $U 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="c0276-107">입력</span><span class="sxs-lookup"><span data-stu-id="c0276-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="c0276-108">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c0276-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c0276-109">반복 될 게이트를 나타내는 연산이 $U입니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="c0276-110">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c0276-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c0276-111">$U $가 반복 되는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="c0276-112">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c0276-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c0276-113">^ M $ $U를 나타내는 새 작업입니다. 여기서 $m = \texttt{power} $입니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c0276-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0276-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c0276-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="c0276-115">'T</span></span>

<span data-ttu-id="c0276-116">켤 작업의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0276-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c0276-117">See Also</span></span>

- [<span data-ttu-id="c0276-118">OperationPowC입니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="c0276-119">OperationPowA입니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="c0276-120">OperationPowCA입니다.</span><span class="sxs-lookup"><span data-stu-id="c0276-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)