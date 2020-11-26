---
uid: Microsoft.Quantum.Simulation.BlockEncodingByLCU
title: BlockEncodingByLCU 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingByLCU
qsharp.summary: >-
  Encodes an operator of interest into a `BlockEncoding`.

  This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries. Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.
ms.openlocfilehash: 254ace01750f94e6c871de9b62f1342000bc84ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229548"
---
# <a name="blockencodingbylcu-function"></a><span data-ttu-id="a1c38-102">BlockEncodingByLCU 함수</span><span class="sxs-lookup"><span data-stu-id="a1c38-102">BlockEncodingByLCU function</span></span>

<span data-ttu-id="a1c38-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a1c38-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a1c38-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a1c38-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a1c38-105">원하는 연산자를로 인코딩합니다 `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="a1c38-105">Encodes an operator of interest into a `BlockEncoding`.</span></span>

<span data-ttu-id="a1c38-106">이는 `BlockEncoding` 단일 $U = P\cdot V\cdot P ^ \kcdot $를 생성 합니다 .이 경우 일부 연산자 $H = \ sum_ {j} | \ alpha_j | Unitaries의 선형 조합 인 관심 U_j $입니다.</span><span class="sxs-lookup"><span data-stu-id="a1c38-106">This constructs a `BlockEncoding` unitary $U=P\cdot V\cdot P^\dagger$ that encodes some operator $H=\sum_{j}|\alpha_j|U_j$ of interest that is a linear combination of unitaries.</span></span> <span data-ttu-id="a1c38-107">일반적으로 $P $은 $P \ket {0} \_ a = \ sum_j \sqrt{\ alpha_j/ \| \vec\alpha \| \_ 2} \ket{j} \_ a $ 및 $V = \ sum_ {j} \ket{j}\bra{j} \_ a\otimes U_j $ 같은 상태 준비의 단일 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a1c38-107">Typically, $P$ is a state preparation unitary such that $P\ket{0}\_a=\sum_j\sqrt{\alpha_j/\|\vec\alpha\|\_2}\ket{j}\_a$, and $V=\sum_{j}\ket{j}\bra{j}\_a\otimes U_j$.</span></span>

```qsharp
function BlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl)) : (('T, 'S) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="a1c38-108">입력</span><span class="sxs-lookup"><span data-stu-id="a1c38-108">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="a1c38-109">statePreparation: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a1c38-109">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a1c38-110">일부 대상 상태를 준비 하는 단일 $P $입니다.</span><span class="sxs-lookup"><span data-stu-id="a1c38-110">A unitary $P$ that prepares some target state.</span></span>


### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="a1c38-111">selector: (' ' ') => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a1c38-111">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a1c38-112">$H $의 unitaries 구성 요소를 인코딩하는 단일 $V $입니다.</span><span class="sxs-lookup"><span data-stu-id="a1c38-112">A unitary $V$ that encodes the component unitaries of $H$.</span></span>



## <a name="output--ts--unit--is-adj--ctl"></a><span data-ttu-id="a1c38-113">출력: (' ' ') => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="a1c38-113">Output : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a1c38-114">단일 $U $는 레지스터에 대해 공동으로 작동 `a` 하며 `s` $H $를 차단 하 고 $U ^ \A턴 = U $를 충족 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c38-114">A unitary $U$ acting jointly on registers `a` and `s` that block- encodes $H$, and satisfies $U^\dagger = U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a1c38-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a1c38-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a1c38-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="a1c38-116">'T</span></span>


### <a name="s"></a><span data-ttu-id="a1c38-117">큐브의</span><span class="sxs-lookup"><span data-stu-id="a1c38-117">'S</span></span>



## <a name="remarks"></a><span data-ttu-id="a1c38-118">설명</span><span class="sxs-lookup"><span data-stu-id="a1c38-118">Remarks</span></span>

<span data-ttu-id="a1c38-119">이 `BlockEncoding` 구현에서는의 속성을 제공 `BlockEncodingReflection` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c38-119">This `BlockEncoding` implementation gives it the properties of a `BlockEncodingReflection`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1c38-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a1c38-120">See Also</span></span>

- [<span data-ttu-id="a1c38-121">Microsoft 양자. 블록 인코딩</span><span class="sxs-lookup"><span data-stu-id="a1c38-121">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="a1c38-122">BlockEncodingReflection.</span><span class="sxs-lookup"><span data-stu-id="a1c38-122">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)