---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: StatePreparationPositiveCoefficients 함수
ms.date: 11/25/2020 12:00:00 AM
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
ms.openlocfilehash: 8f1fd7d77531996faf566adb78f452929d6cbd50
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193253"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="f635d-102">StatePreparationPositiveCoefficients 함수</span><span class="sxs-lookup"><span data-stu-id="f635d-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="f635d-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="f635d-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="f635d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f635d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="f635d-105">StatePreparationPositiveCoefficients는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="f635d-106">대신 <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="f635d-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="f635d-107">지정 된 퀀텀 상태를 준비 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="f635d-108">$ $U 반환 되는 작업은 $ \ket{0...0} $ $n $ \ alpha_j \ge $0 인 긍정 계수 $ \ket{\psi} $를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="f635d-109">새로 할당 된 레지스터의 U 동작은 $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="f635d-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="f635d-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="f635d-111">입력</span><span class="sxs-lookup"><span data-stu-id="f635d-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="f635d-112">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f635d-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f635d-113">최대 $2 ^ n $ 계수 $ \ alpha_j $의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="f635d-114">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="f635d-115">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="f635d-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f635d-116">상태 준비 단일 작업 $U $.</span><span class="sxs-lookup"><span data-stu-id="f635d-116">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="f635d-117">설명</span><span class="sxs-lookup"><span data-stu-id="f635d-117">Remarks</span></span>

<span data-ttu-id="f635d-118">음수 입력 계수 $ \ alpha_j < $0는 값 $ | \ alpha_j | $를 사용 하는 긍정으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-118">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="f635d-119">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 $ \ alpha_j = $0.0 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="f635d-119">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>