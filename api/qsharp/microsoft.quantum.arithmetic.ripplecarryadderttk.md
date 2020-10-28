---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderTTK
title: RippleCarryAdderTTK 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers. Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.
ms.openlocfilehash: 5366ace36e63d361a439bfc5a1a78fdf9a353062
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719564"
---
# <a name="ripplecarryadderttk-operation"></a><span data-ttu-id="9f20c-102">RippleCarryAdderTTK 작업</span><span class="sxs-lookup"><span data-stu-id="9f20c-102">RippleCarryAdderTTK operation</span></span>

<span data-ttu-id="9f20c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9f20c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9f20c-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9f20c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9f20c-105">해독 가능한 내부 ripple-두 개의 정수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f20c-105">Reversible, in-place ripple-carry addition of two integers.</span></span>
<span data-ttu-id="9f20c-106">LittleEndian 레지스터 및에서 인코딩된 두 개의 $n $ bit 정수를 제공 하 `xs` `ys` 고,이 작업은 두 정수의 합계를 계산 하며,이는 결과의 $n $ 최하위 비트를 유지 하 `ys` 고, 운반 비트를 xored 하는 것입니다 `carry` .</span><span class="sxs-lookup"><span data-stu-id="9f20c-106">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, and a qubit carry, the operation computes the sum of the two integers where the $n$ least significant bits of the result are held in `ys` and the carry out bit is xored to the qubit `carry`.</span></span>

```qsharp
operation RippleCarryAdderTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="9f20c-107">입력</span><span class="sxs-lookup"><span data-stu-id="9f20c-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="9f20c-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9f20c-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9f20c-109">LittleEndian cobit는 첫 번째 정수 summand을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f20c-109">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="9f20c-110">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9f20c-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9f20c-111">LittleEndian의 두 번째 정수 summand는 sum의 $n $ 최하위 비트를 포함 하도록 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9f20c-111">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="9f20c-112">운반: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9f20c-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9f20c-113">Xored은 합계의 가장 중요 한 비트를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f20c-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9f20c-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f20c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9f20c-115">설명</span><span class="sxs-lookup"><span data-stu-id="9f20c-115">Remarks</span></span>

<span data-ttu-id="9f20c-116">이 작업에는 RippleCarryAdderD 및, RippleCarryAdderCDKM와 동일한 기능이 있지만 ancilla any 비트는 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f20c-116">This operation has the same functionality as RippleCarryAdderD and, RippleCarryAdderCDKM but does not use any ancilla qubits.</span></span>

## <a name="references"></a><span data-ttu-id="9f20c-117">참조</span><span class="sxs-lookup"><span data-stu-id="9f20c-117">References</span></span>

- <span data-ttu-id="9f20c-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "퀀텀 추가 회로 및 무제한 팬 아웃", 퀀텀 정보 및 계산, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="9f20c-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530