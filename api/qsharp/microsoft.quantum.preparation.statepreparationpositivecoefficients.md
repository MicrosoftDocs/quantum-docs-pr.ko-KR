---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: StatePreparationPositiveCoefficients 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 39d961c71d231e7b51290f81c20c8c6b48c7e0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722895"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="7d972-102">StatePreparationPositiveCoefficients 함수</span><span class="sxs-lookup"><span data-stu-id="7d972-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="7d972-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7d972-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7d972-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7d972-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7d972-105">지정 된 퀀텀 상태를 준비 하는 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d972-105">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="7d972-106">$ $U 반환 되는 작업은 $ \ket{0...0} $ $n $ \ alpha_j \ge $0 인 긍정 계수 $ \ket{\psi} $를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d972-106">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="7d972-107">새로 할당 된 레지스터의 U 동작은 $ $ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \ket{j}}{\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}에 의해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d972-107">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="7d972-108">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="7d972-108">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="7d972-109">입력</span><span class="sxs-lookup"><span data-stu-id="7d972-109">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="7d972-110">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="7d972-110">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="7d972-111">최대 $2 ^ n $ 계수 $ \ alpha_j $의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="7d972-111">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="7d972-112">$J $ th 계수는 작은 endian 형식으로 인코딩된 number state $ \ket{j} $를 인덱싱합니다.</span><span class="sxs-lookup"><span data-stu-id="7d972-112">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit-adj--ctl"></a><span data-ttu-id="7d972-113">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="7d972-113">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="7d972-114">상태 준비 단일 작업 $U $.</span><span class="sxs-lookup"><span data-stu-id="7d972-114">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d972-115">설명</span><span class="sxs-lookup"><span data-stu-id="7d972-115">Remarks</span></span>

<span data-ttu-id="7d972-116">음수 입력 계수 $ \ alpha_j < $0는 값 $ | \ alpha_j | $를 사용 하는 긍정으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d972-116">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="7d972-117">`coefficients` $2 ^ n $ 미만으로 지정 된 경우는 $ \ alpha_j = $0.0 요소로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="7d972-117">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>