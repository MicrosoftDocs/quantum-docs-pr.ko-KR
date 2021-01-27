---
uid: Microsoft.Quantum.Canon.OperationPowA
title: OperationPowA 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 67491c3302392e9793677727606df1baaf4f205a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852363"
---
# <a name="operationpowa-function"></a><span data-ttu-id="77e14-102">OperationPowA 함수</span><span class="sxs-lookup"><span data-stu-id="77e14-102">OperationPowA function</span></span>

<span data-ttu-id="77e14-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="77e14-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="77e14-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77e14-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77e14-105">전원에 대 한 작업을 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-105">Raises an operation to a power.</span></span>
<span data-ttu-id="77e14-106">한정자는 `A` 작업이 adjointable를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-106">The modifier `A` indicates that the operation is adjointable.</span></span>

<span data-ttu-id="77e14-107">즉, $ $U $를 나타내는 작업이 지정 된 경우 power $m $에 대해 ^ m $ $U 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="77e14-108">입력</span><span class="sxs-lookup"><span data-stu-id="77e14-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="77e14-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="77e14-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="77e14-110">반복 될 게이트를 나타내는 연산이 $U입니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="77e14-111">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="77e14-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="77e14-112">$U $가 반복 되는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-adj"></a><span data-ttu-id="77e14-113">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span><span class="sxs-lookup"><span data-stu-id="77e14-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="77e14-114">^ M $ $U를 나타내는 새 작업입니다. 여기서 $m = \texttt{power} $입니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="77e14-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="77e14-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="77e14-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="77e14-116">'T</span></span>

<span data-ttu-id="77e14-117">켤 작업의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="77e14-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="77e14-118">See Also</span></span>

- [<span data-ttu-id="77e14-119">OperationPow입니다.</span><span class="sxs-lookup"><span data-stu-id="77e14-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)