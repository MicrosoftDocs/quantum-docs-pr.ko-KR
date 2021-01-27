---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: StatePreparationComplexCoefficients 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationComplexCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: c16df0fe075b15cff745a6b7d5b79aac39c14d09
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856130"
---
# <a name="statepreparationcomplexcoefficients-function"></a><span data-ttu-id="09fc6-102">StatePreparationComplexCoefficients 함수</span><span class="sxs-lookup"><span data-stu-id="09fc6-102">StatePreparationComplexCoefficients function</span></span>

<span data-ttu-id="09fc6-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="09fc6-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="09fc6-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09fc6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="09fc6-105">StatePreparationComplexCoefficients는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-105">StatePreparationComplexCoefficients has been deprecated.</span></span> <span data-ttu-id="09fc6-106">대신 <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="09fc6-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="09fc6-107">특정 퀀텀 상태를 준비 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-107">Returns an operation that prepares a specific quantum state.</span></span>

<span data-ttu-id="09fc6-108">반환 된 작업 $U $은 $n $-\ket{0...0} $에서 t_j e ^ {i} $ 복합 _j $r 계수를 사용 하 여 임의의 퀀텀 상태 $ \ket{\psi} $을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="09fc6-109">새로 할당 된 레지스터의 U 동작은 $ $ \begin{align} U\ket {0 ... 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-109">The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}.</span></span>
<span data-ttu-id="09fc6-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="09fc6-110">\end{align} $$</span></span>

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="09fc6-111">입력</span><span class="sxs-lookup"><span data-stu-id="09fc6-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="09fc6-112">계수: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="09fc6-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="09fc6-113">절대 값으로 표현 되는 $2 ^ n $ 복합 계수와 $ (r_j, t_j) $ 단계로 이루어진 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="09fc6-114">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="09fc6-115">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="09fc6-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="09fc6-116">상태 준비 단일 작업 $U $.</span><span class="sxs-lookup"><span data-stu-id="09fc6-116">A state-preparation unitary operation $U$.</span></span>

## <a name="example"></a><span data-ttu-id="09fc6-117">예</span><span class="sxs-lookup"><span data-stu-id="09fc6-117">Example</span></span>

<span data-ttu-id="09fc6-118">다음 코드 조각은 stbit 레지스터에서 퀀텀 상태 $ \ket{\psi} = e ^ {i 0.1} \ sqrt {1/8} \ k {0} + \ sqrt {7/8} \ k $를 준비 합니다 {2} `qubitsLE` .</span><span class="sxs-lookup"><span data-stu-id="09fc6-118">The following snippet prepares the quantum state $\ket{\psi}=e^{i 0.1}\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{2}$ in the qubit register `qubitsLE`.</span></span>

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let phases = [0.1, 0.0, 0.0, 0.0];
mutable complexNumbers = new ComplexPolar[4];
for (idx in 0..3) {
    set complexNumbers[idx] = ComplexPolar(amplitudes[idx], phases[idx]);
}
let op = StatePreparationComplexCoefficients(complexNumbers);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a><span data-ttu-id="09fc6-119">설명</span><span class="sxs-lookup"><span data-stu-id="09fc6-119">Remarks</span></span>

<span data-ttu-id="09fc6-120">음수 입력 계수 $r _j < $0는 값 $ | r_j | $로 긍정으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="09fc6-121">`coefficients` $2 ^ n $ 보다 작은 경우는 $ (r_j, t_j) = (0.0, 0.0) $ 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="09fc6-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>