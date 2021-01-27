---
uid: Microsoft.Quantum.Canon.OperationPow
title: OperationPow 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 9ed0d32c084f183527cac0586ad699417f51df29
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852374"
---
# <a name="operationpow-function"></a><span data-ttu-id="4e7f6-102">OperationPow 함수</span><span class="sxs-lookup"><span data-stu-id="4e7f6-102">OperationPow function</span></span>

<span data-ttu-id="4e7f6-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4e7f6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4e7f6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4e7f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4e7f6-105">전원에 대 한 작업을 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-105">Raises an operation to a power.</span></span>

<span data-ttu-id="4e7f6-106">즉, $ $U $를 나타내는 작업이 지정 된 경우 power $m $에 대해 ^ m $ $U 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="4e7f6-107">입력</span><span class="sxs-lookup"><span data-stu-id="4e7f6-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="4e7f6-108">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e7f6-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4e7f6-109">반복 될 게이트를 나타내는 연산이 $U입니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="4e7f6-110">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4e7f6-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4e7f6-111">$U $가 반복 되는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="4e7f6-112">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4e7f6-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="4e7f6-113">^ M $ $U를 나타내는 새 작업입니다. 여기서 $m = \texttt{power} $입니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4e7f6-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4e7f6-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4e7f6-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="4e7f6-115">'T</span></span>

<span data-ttu-id="4e7f6-116">켤 작업의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e7f6-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4e7f6-117">See Also</span></span>

- [<span data-ttu-id="4e7f6-118">OperationPowC입니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="4e7f6-119">OperationPowA입니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="4e7f6-120">OperationPowCA입니다.</span><span class="sxs-lookup"><span data-stu-id="4e7f6-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)