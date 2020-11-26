---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: RippleCarryAdderNoCarryTTK 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: a539d85a4800c2f4452a1c6fe2c4f88a6296c3e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222000"
---
# <a name="ripplecarryaddernocarryttk-operation"></a><span data-ttu-id="b1ce7-102">RippleCarryAdderNoCarryTTK 작업</span><span class="sxs-lookup"><span data-stu-id="b1ce7-102">RippleCarryAdderNoCarryTTK operation</span></span>

<span data-ttu-id="b1ce7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b1ce7-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b1ce7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b1ce7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b1ce7-105">해독 가능, 내부 ripple-수행 하지 않고 두 개의 정수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ce7-105">Reversible, in-place ripple-carry addition of two integers without carry out.</span></span>

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="b1ce7-106">Description</span><span class="sxs-lookup"><span data-stu-id="b1ce7-106">Description</span></span>

<span data-ttu-id="b1ce7-107">LittleEndian 레지스터 및에서 인코딩된 두 개의 $n $ bit 정수를 지정 하면 `xs` `ys` 연산은 두 정수 모듈로 $2 ^ n $의 합계를 계산 합니다. 여기서 $n $는 입력 및의 비트 크기입니다 `xs` `ys` .</span><span class="sxs-lookup"><span data-stu-id="b1ce7-107">Given two $n$-bit integers encoded in LittleEndian registers `xs` and `ys`, the operation computes the sum of the two integers modulo $2^n$, where $n$ is the bit size of the inputs `xs` and `ys`.</span></span> <span data-ttu-id="b1ce7-108">이는 운반 비트를 계산 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1ce7-108">It does not compute the carry out bit.</span></span>

## <a name="input"></a><span data-ttu-id="b1ce7-109">입력</span><span class="sxs-lookup"><span data-stu-id="b1ce7-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="b1ce7-110">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b1ce7-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b1ce7-111">LittleEndian cobit는 첫 번째 정수 summand을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1ce7-111">LittleEndian qubit register encoding the first integer summand.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="b1ce7-112">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b1ce7-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b1ce7-113">LittleEndian의 두 번째 정수 summand는 sum의 $n $ 최하위 비트를 포함 하도록 수정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b1ce7-113">LittleEndian qubit register encoding the second integer summand, is modified to hold the $n$ least significant bits of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b1ce7-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b1ce7-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b1ce7-115">설명</span><span class="sxs-lookup"><span data-stu-id="b1ce7-115">Remarks</span></span>

<span data-ttu-id="b1ce7-116">이 작업은 RippleCarryAdderTTK와 동일한 기능을 수행 하지만 운반 비트를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1ce7-116">This operation has the same functionality as RippleCarryAdderTTK but does not return the carry bit.</span></span>

## <a name="references"></a><span data-ttu-id="b1ce7-117">참조 항목</span><span class="sxs-lookup"><span data-stu-id="b1ce7-117">References</span></span>

- <span data-ttu-id="b1ce7-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "퀀텀 추가 회로 및 무제한 팬 아웃", 퀀텀 정보 및 계산, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="b1ce7-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530