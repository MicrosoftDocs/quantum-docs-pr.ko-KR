---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: ApplyInnerTTKAdderWithoutCarry 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 3335c63b8509090deed1172419158da0d5e80409
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721645"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a><span data-ttu-id="1bcc0-102">ApplyInnerTTKAdderWithoutCarry 작업</span><span class="sxs-lookup"><span data-stu-id="1bcc0-102">ApplyInnerTTKAdderWithoutCarry operation</span></span>

<span data-ttu-id="1bcc0-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1bcc0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1bcc0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1bcc0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1bcc0-105">RippleCarryAdderNoCarryTTK 작업에 대 한 내부 더하기 함수를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bcc0-105">Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK.</span></span> <span data-ttu-id="1bcc0-106">이 작업은 전체 adder를 생성 하는 외부 작업과 conjugated 된 내부 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1bcc0-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="1bcc0-107">입력</span><span class="sxs-lookup"><span data-stu-id="1bcc0-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="1bcc0-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1bcc0-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1bcc0-109">LittleEndian cobit summand 입력을 RippleCarryAdderNoCarryTTK에 첫 번째 정수를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bcc0-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderNoCarryTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="1bcc0-110">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1bcc0-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1bcc0-111">LittleEndian cobit는 두 번째 정수 summand 입력을 RippleCarryAdderNoCarryTTK에 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bcc0-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderNoCarryTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1bcc0-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1bcc0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="1bcc0-113">설명</span><span class="sxs-lookup"><span data-stu-id="1bcc0-113">Remarks</span></span>

<span data-ttu-id="1bcc0-114">지정 된 제어 작업을 통해 작업의 대칭 및 상호 취소를 사용 하 여 모든 작업에 컨트롤을 추가 하는 기본 구현을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bcc0-114">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="1bcc0-115">참조</span><span class="sxs-lookup"><span data-stu-id="1bcc0-115">References</span></span>

- <span data-ttu-id="1bcc0-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "퀀텀 추가 회로 및 무제한 팬 아웃", 퀀텀 정보 및 계산, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="1bcc0-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530