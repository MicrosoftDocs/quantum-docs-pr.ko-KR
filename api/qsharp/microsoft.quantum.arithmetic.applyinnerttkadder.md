---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdder
title: ApplyInnerTTKAdder 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdder
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 1de0248066aec531d78130703414067603ffd34d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191009"
---
# <a name="applyinnerttkadder-operation"></a><span data-ttu-id="78c92-102">ApplyInnerTTKAdder 작업</span><span class="sxs-lookup"><span data-stu-id="78c92-102">ApplyInnerTTKAdder operation</span></span>

<span data-ttu-id="78c92-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="78c92-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="78c92-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="78c92-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="78c92-105">RippleCarryAdderTTK 작업에 대 한 내부 더하기 함수를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c92-105">Implements the inner addition function for the operation RippleCarryAdderTTK.</span></span> <span data-ttu-id="78c92-106">이 작업은 전체 adder를 생성 하는 외부 작업과 conjugated 된 내부 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="78c92-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="78c92-107">입력</span><span class="sxs-lookup"><span data-stu-id="78c92-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="78c92-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="78c92-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="78c92-109">LittleEndian cobit summand 입력을 RippleCarryAdderTTK에 첫 번째 정수를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c92-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="78c92-110">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="78c92-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="78c92-111">LittleEndian cobit는 두 번째 정수 summand 입력을 RippleCarryAdderTTK에 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c92-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="78c92-112">운반: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="78c92-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="78c92-113">Xored은 합계의 가장 중요 한 비트를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78c92-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="78c92-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="78c92-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="78c92-115">설명</span><span class="sxs-lookup"><span data-stu-id="78c92-115">Remarks</span></span>

<span data-ttu-id="78c92-116">지정 된 제어 작업을 통해 작업의 대칭 및 상호 취소를 사용 하 여 모든 작업에 컨트롤을 추가 하는 기본 구현을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c92-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="78c92-117">참조 항목</span><span class="sxs-lookup"><span data-stu-id="78c92-117">References</span></span>

- <span data-ttu-id="78c92-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "퀀텀 추가 회로 및 무제한 팬 아웃", 퀀텀 정보 및 계산, Vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="78c92-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530