---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderCDKM
title: RippleCarryAdderCDKM 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderCDKM
qsharp.summary: Reversible, in-place ripple-carry addition of two integers.
ms.openlocfilehash: df9b62b649af532a4202aacc3e8dd4613eb8665d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846353"
---
# <a name="ripplecarryaddercdkm-operation"></a><span data-ttu-id="80d2b-102">RippleCarryAdderCDKM 작업</span><span class="sxs-lookup"><span data-stu-id="80d2b-102">RippleCarryAdderCDKM operation</span></span>

<span data-ttu-id="80d2b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="80d2b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="80d2b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="80d2b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="80d2b-105">해독 가능한 내부 ripple-두 개의 정수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d2b-105">Reversible, in-place ripple-carry addition of two integers.</span></span>

```qsharp
operation RippleCarryAdderCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="80d2b-106">설명</span><span class="sxs-lookup"><span data-stu-id="80d2b-106">Description</span></span>

<span data-ttu-id="80d2b-107">LittleEndian 레지스터 및에서 인코딩된 두 개의 $n $ bit 정수를 제공 하 `xs` `ys` 고,이 작업은 두 정수의 합계를 계산 하며,이는 결과의 $n $ 최하위 비트를 유지 하 `ys` 고, 운반 비트를 xored 하는 것입니다 `carry` .</span><span class="sxs-lookup"><span data-stu-id="80d2b-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

## <a name="input"></a><span data-ttu-id="80d2b-108">입력</span><span class="sxs-lookup"><span data-stu-id="80d2b-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="80d2b-109">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="80d2b-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="80d2b-110">LittleEndian cobit는 첫 번째 정수 summand을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d2b-110">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="80d2b-111">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="80d2b-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="80d2b-112">LittleEndian의 두 번째 정수 summand는 sum의 최하위 비트를 포함 하도록 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80d2b-112">LittleEndian qubit register encoding the second integer summand, is modified to hold the n least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="80d2b-113">운반: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="80d2b-113">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="80d2b-114">Xored은 합계의 가장 중요 한 비트를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80d2b-114">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="80d2b-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="80d2b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="80d2b-116">설명</span><span class="sxs-lookup"><span data-stu-id="80d2b-116">Remarks</span></span>

<span data-ttu-id="80d2b-117">이 작업은 RippleCarryAdderD와 동일한 기능을 포함 하지만 $n $ 대신 하나의 보조 비트만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d2b-117">This operation has the same functionality as RippleCarryAdderD, but only uses one auxiliary qubit instead of $n$.</span></span>

## <a name="references"></a><span data-ttu-id="80d2b-118">참조</span><span class="sxs-lookup"><span data-stu-id="80d2b-118">References</span></span>

- <span data-ttu-id="80d2b-119">Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new 퀀텀 ripple and A new, 2004.</span><span class="sxs-lookup"><span data-stu-id="80d2b-119">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1