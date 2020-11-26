---
uid: Microsoft.Quantum.Arithmetic.Sum
title: 합계(Sum) 연산
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: 7758e29c9f08f4d05253defbe5a43a5316289522
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221796"
---
# <a name="sum-operation"></a><span data-ttu-id="5b444-102">합계(Sum) 연산</span><span class="sxs-lookup"><span data-stu-id="5b444-102">Sum operation</span></span>

<span data-ttu-id="5b444-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5b444-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5b444-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5b444-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5b444-105">해독 가능한 sum gate를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b444-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="5b444-106">에서로 인코딩된 전달 비트 `carryIn` 와 및에서 인코딩된 두 개의 summand 비트가 지정 된 경우 `summand1` 는 `summand2` 의 비트 xor를 계산 합니다 `carryIn` `summand1` `summand2` `summand2` .</span><span class="sxs-lookup"><span data-stu-id="5b444-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5b444-107">입력</span><span class="sxs-lookup"><span data-stu-id="5b444-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="5b444-108">carryIn: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b444-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b444-109">운반 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="5b444-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="5b444-110">summand1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b444-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b444-111">첫 번째 summand입니다.</span><span class="sxs-lookup"><span data-stu-id="5b444-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="5b444-112">summand2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b444-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b444-113">두 번째 summand는 및의 합계에서 하위 비트를 대체 합니다 `summand1` `summand2` .</span><span class="sxs-lookup"><span data-stu-id="5b444-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b444-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b444-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5b444-115">설명</span><span class="sxs-lookup"><span data-stu-id="5b444-115">Remarks</span></span>

<span data-ttu-id="5b444-116">`Carry`작업과 달리이 작업은 실행 비트를 계산 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b444-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>