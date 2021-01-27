---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: StatePreparationPositiveCoefficients 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855854"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="acc8b-102">StatePreparationPositiveCoefficients 함수</span><span class="sxs-lookup"><span data-stu-id="acc8b-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="acc8b-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="acc8b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="acc8b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="acc8b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="acc8b-105">StatePreparationPositiveCoefficients는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="acc8b-106">대신 <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="acc8b-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="acc8b-107">지정 된 퀀텀 상태를 준비 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="acc8b-108">$ $U 반환 되는 작업은 $ \ket{0...0} $ $n $ \ alpha_j \ge $0 인 긍정 계수 $ \ket{\psi} $를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="acc8b-109">새로 할당 된 레지스터의 U 동작은 $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="acc8b-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="acc8b-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="acc8b-111">입력</span><span class="sxs-lookup"><span data-stu-id="acc8b-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="acc8b-112">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="acc8b-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="acc8b-113">최대 $2 ^ n $ 계수 $ \ alpha_j $의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="acc8b-114">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="acc8b-115">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="acc8b-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="acc8b-116">상태 준비 단일 작업 $U $.</span><span class="sxs-lookup"><span data-stu-id="acc8b-116">A state-preparation unitary operation $U$.</span></span>

## <a name="example"></a><span data-ttu-id="acc8b-117">예</span><span class="sxs-lookup"><span data-stu-id="acc8b-117">Example</span></span>

<span data-ttu-id="acc8b-118">다음 코드 조각은 stbit 레지스터에서 퀀텀 상태 $ \ket{\psi} = \ sqrt {1/8} \ k {0} + \ sqrt {7/8} \ k $를 준비 합니다 {2} `qubitsLE` .</span><span class="sxs-lookup"><span data-stu-id="acc8b-118">The following snippet prepares the quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{2}$ in the qubit register `qubitsLE`.</span></span>

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a><span data-ttu-id="acc8b-119">설명</span><span class="sxs-lookup"><span data-stu-id="acc8b-119">Remarks</span></span>

<span data-ttu-id="acc8b-120">음수 입력 계수 $ \ alpha_j < $0는 값 $ | \ alpha_j | $를 사용 하는 긍정으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-120">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="acc8b-121">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 $ \ alpha_j = $0.0 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="acc8b-121">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>