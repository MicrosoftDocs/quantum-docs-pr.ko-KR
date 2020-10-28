---
uid: Microsoft.Quantum.Arithmetic.Carry
title: 작업 수행
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: 2b977151861fb01be7d7dbad6e0a7b803fded880
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721309"
---
# <a name="carry-operation"></a><span data-ttu-id="50f76-102">작업 수행</span><span class="sxs-lookup"><span data-stu-id="50f76-102">Carry operation</span></span>

<span data-ttu-id="50f76-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="50f76-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="50f76-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="50f76-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="50f76-105">해독 가능한 전달 게이트를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="50f76-105">Implements a reversible carry gate.</span></span> <span data-ttu-id="50f76-106">에서로 인코딩된 전달 비트 `carryIn` 와 및에서 인코딩된 두 개의 summand 비트가 지정 된 경우 `summand1` `summand2` ,는의 비트 xor를 계산 하 고,는이 비트의 비트 xor를 계산 `carryIn` `summand1` `summand2` `summand2` 합니다 `carryOut` .</span><span class="sxs-lookup"><span data-stu-id="50f76-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.</span></span>

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="50f76-107">입력</span><span class="sxs-lookup"><span data-stu-id="50f76-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="50f76-108">carryIn: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="50f76-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="50f76-109">운반 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="50f76-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="50f76-110">summand1: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="50f76-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="50f76-111">첫 번째 summand입니다.</span><span class="sxs-lookup"><span data-stu-id="50f76-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="50f76-112">summand2: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="50f76-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="50f76-113">두 번째 summand는 및의 합계에서 하위 비트를 대체 합니다 `summand1` `summand2` .</span><span class="sxs-lookup"><span data-stu-id="50f76-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>


### <a name="carryout--qubit"></a><span data-ttu-id="50f76-114">carryOut: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="50f76-114">carryOut : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="50f76-115">수행 하는 것은 합계의 상위 비트를 사용 하 여 xored 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f76-115">Carry-out qubit, will be xored with the higher bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="50f76-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="50f76-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

