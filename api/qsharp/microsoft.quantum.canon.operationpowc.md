---
uid: Microsoft.Quantum.Canon.OperationPowC
title: OperationPowC 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 71f66dd0098ab58d327fc33dbe5af191df0d3dc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205731"
---
# <a name="operationpowc-function"></a><span data-ttu-id="cab21-102">OperationPowC 함수</span><span class="sxs-lookup"><span data-stu-id="cab21-102">OperationPowC function</span></span>

<span data-ttu-id="cab21-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cab21-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cab21-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cab21-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cab21-105">전원에 대 한 작업을 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-105">Raises an operation to a power.</span></span>
<span data-ttu-id="cab21-106">한정자는 `C` 작업을 제어할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-106">The modifier `C` indicates that the operation is controllable.</span></span>

<span data-ttu-id="cab21-107">즉, $ $U $를 나타내는 작업이 지정 된 경우 power $m $에 대해 ^ m $ $U 새 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="cab21-108">입력</span><span class="sxs-lookup"><span data-stu-id="cab21-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="cab21-109">op: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="cab21-110">반복 될 게이트를 나타내는 연산이 $U입니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="cab21-111">power: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cab21-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cab21-112">$U $가 반복 되는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit--is-ctl"></a><span data-ttu-id="cab21-113">출력: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="cab21-114">^ M $ $U를 나타내는 새 작업입니다. 여기서 $m = \texttt{power} $입니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cab21-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cab21-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cab21-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="cab21-116">'T</span></span>

<span data-ttu-id="cab21-117">켤 작업의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="cab21-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cab21-118">See Also</span></span>

- [<span data-ttu-id="cab21-119">OperationPow입니다.</span><span class="sxs-lookup"><span data-stu-id="cab21-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)