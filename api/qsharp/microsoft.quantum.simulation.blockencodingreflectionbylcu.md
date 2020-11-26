---
uid: Microsoft.Quantum.Simulation.BlockEncodingReflectionByLCU
title: BlockEncodingReflectionByLCU 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingReflectionByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncodingReflection`.

  This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: e1247d961a7ebce798106c24c46d924dd6e6d347
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229480"
---
# <a name="blockencodingreflectionbylcu-function"></a><span data-ttu-id="4aac5-102">BlockEncodingReflectionByLCU 함수</span><span class="sxs-lookup"><span data-stu-id="4aac5-102">BlockEncodingReflectionByLCU function</span></span>

<span data-ttu-id="4aac5-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4aac5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4aac5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4aac5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4aac5-105">원하는 연산자를로 인코딩합니다 `BlockEncodingReflection` .</span><span class="sxs-lookup"><span data-stu-id="4aac5-105">Encodes an operator of interest into a `BlockEncodingReflection`.</span></span>

<span data-ttu-id="4aac5-106">이는 `BlockEncodingReflection` 단일 $U = P\cdot V\cdot P ^ \kcdot $를 생성 합니다 .이 경우 일부 연산자 $H = \ sum_ {j} | \ alpha_j | Unitaries의 선형 조합 인 관심 U_j $입니다.</span><span class="sxs-lookup"><span data-stu-id="4aac5-106">This constructs a `BlockEncodingReflection` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="4aac5-107">일반적으로 $P $은 $P \ket {0} \_ a \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ 및 $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $ 같은 상태 준비의 단일입니다.</span><span class="sxs-lookup"><span data-stu-id="4aac5-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingReflectionByLCU (statePreparation : (Qubit[] => Unit is Adj + Ctl), selector : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a><span data-ttu-id="4aac5-108">입력</span><span class="sxs-lookup"><span data-stu-id="4aac5-108">Input</span></span>

### <a name="statepreparation--qubit--unit--is-adj--ctl"></a><span data-ttu-id="4aac5-109">statePreparation: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="4aac5-109">statePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4aac5-110">일부 대상 상태를 준비 하는 단일 $P $입니다.</span><span class="sxs-lookup"><span data-stu-id="4aac5-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="4aac5-111">selector: (추가[비트](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => [Unit](xref:microsoft.quantum.lang-ref.unit) is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="4aac5-111">selector : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4aac5-112">$H $의 unitaries 구성 요소를 인코딩하는 단일 $V $입니다.</span><span class="sxs-lookup"><span data-stu-id="4aac5-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--blockencodingreflection"></a><span data-ttu-id="4aac5-113">출력: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="4aac5-113">Output : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="4aac5-114">단일 $U $는 레지스터에 대해 공동으로 작동 `a` 하며 `s` $H $를 차단 하 고 $U ' ^ {-1} = U $를 충족 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aac5-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U'^{-1} = U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aac5-115">설명</span><span class="sxs-lookup"><span data-stu-id="4aac5-115">Remarks</span></span>

<span data-ttu-id="4aac5-116">이 `BlockEncoding` 구현에서는의 속성을 제공 `BlockEncodingReflection` 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aac5-116">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4aac5-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4aac5-117">See Also</span></span>

- [<span data-ttu-id="4aac5-118">Microsoft 양자. 블록 인코딩</span><span class="sxs-lookup"><span data-stu-id="4aac5-118">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="4aac5-119">BlockEncodingReflection.</span><span class="sxs-lookup"><span data-stu-id="4aac5-119">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)