---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderD
title: RippleCarryAdderD 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderD
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: c4466feebb8ff6afcdcb5bf385ec10e807c00537
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719588"
---
# <a name="ripplecarryadderd-operation"></a><span data-ttu-id="b78ed-102">RippleCarryAdderD 작업</span><span class="sxs-lookup"><span data-stu-id="b78ed-102">RippleCarryAdderD operation</span></span>

<span data-ttu-id="b78ed-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b78ed-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b78ed-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b78ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b78ed-105">해독 가능한 내부 ripple-두 개의 정수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78ed-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="b78ed-106">LittleEndian 레지스터 및에서 인코딩된 두 개의 $n $ bit 정수를 제공 하 `xs` `ys` 고,이 작업은 두 정수의 합계를 계산 하며,이는 결과의 $n $ 최하위 비트를 유지 하 `ys` 고, 운반 비트를 xored 하는 것입니다 `carry` .</span><span class="sxs-lookup"><span data-stu-id="b78ed-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderD (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="b78ed-107">입력</span><span class="sxs-lookup"><span data-stu-id="b78ed-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="b78ed-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b78ed-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b78ed-109">LittleEndian cobit는 첫 번째 정수 summand을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78ed-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="b78ed-110">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b78ed-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b78ed-111">LittleEndian의 두 번째 정수 summand는 sum의 $n $ 최하위 비트를 포함 하도록 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b78ed-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="b78ed-112">운반: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b78ed-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b78ed-113">Xored은 합계의 가장 중요 한 비트를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b78ed-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b78ed-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b78ed-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b78ed-115">설명</span><span class="sxs-lookup"><span data-stu-id="b78ed-115">Remarks</span></span>

<span data-ttu-id="b78ed-116">지정 된 제어 작업을 통해 작업의 대칭 및 상호 취소를 사용 하 여 모든 작업에 컨트롤을 추가 하는 기본 구현을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78ed-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="b78ed-117">참조</span><span class="sxs-lookup"><span data-stu-id="b78ed-117">References</span></span>

- <span data-ttu-id="b78ed-118">Thomas G. Draper: "퀀텀 컴퓨터에 추가", 2000.</span><span class="sxs-lookup"><span data-stu-id="b78ed-118">Thomas G. Draper: "Addition on a Quantum Computer", 2000.</span></span>
  https://arxiv.org/abs/quant-ph/0008033