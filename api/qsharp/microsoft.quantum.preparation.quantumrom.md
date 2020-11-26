---
uid: Microsoft.Quantum.Preparation.QuantumROM
title: QuantumROM 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROM
qsharp.summary: >-
  > [!WARNING]

  > QuantumROM has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.


  Uses the Quantum ROM technique to represent a given density matrix.

  Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$. In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$. In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}. \end{align} $$
ms.openlocfilehash: 1ee805fb2ea02121daaab7fc3eb5dbbcb134b470
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229888"
---
# <a name="quantumrom-function"></a><span data-ttu-id="5366a-102">QuantumROM 함수</span><span class="sxs-lookup"><span data-stu-id="5366a-102">QuantumROM function</span></span>

<span data-ttu-id="5366a-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="5366a-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="5366a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5366a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="5366a-105">QuantumROM는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-105">QuantumROM has been deprecated.</span></span> <span data-ttu-id="5366a-106">대신 <xref:Microsoft.Quantum.Preparation.PurifiedMixedState>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="5366a-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedState> instead.</span></span>

<span data-ttu-id="5366a-107">는 퀀텀 ROM 기술을 사용 하 여 지정 된 밀도 행렬을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-107">Uses the Quantum ROM technique to represent a given density matrix.</span></span>

<span data-ttu-id="5366a-108">$ 계수의 $ \ alpha_j $ $N 목록이 지정 된 경우,이는 \ket{j}\bra{j} 기술을 사용 하 여 밀도 행렬 $ \rho = \ p_j {j = 0} ^ {N-1} \frac{| sum_ |}의 purification에 대 한 근사치 $ \tilde\rho\ sum_ {j = 0} ^ {N-1} alpha_j $를 준비 하는 단일 $U $를 반환 합니다. {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $.</span><span class="sxs-lookup"><span data-stu-id="5366a-108">Given a list of $N$ coefficients $\alpha_j$, this returns a unitary $U$ that uses the Quantum-ROM technique to prepare an approximation  $\tilde\rho\sum_{j=0}^{N-1}p_j\ket{j}\bra{j}$ of the purification of the density matrix $\rho=\sum_{j=0}^{N-1}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$.</span></span> <span data-ttu-id="5366a-109">이러한 근사값에서 $ \epsilon $ 오류는 $ | p_j-\frac{| alpha_j |}입니다. {\ sum_k | \ alpha_k |} | \le \le/N $ 및 $ \| \tilde\rho-\rho \| \le \te\e $를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-109">In this approximation, the error $\epsilon$ is such that $|p_j-\frac{|alpha_j|}{\sum_k |\alpha_k|}|\le \epsilon / N$ and $\|\tilde\rho - \rho\| \le \epsilon$.</span></span> <span data-ttu-id="5366a-110">즉, $ $ \begin{align} U\ket {0} ^ {\lceil\ log_2 N\rceil} \ k {0} ^ {m} = \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage} _j}입니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-110">In other words, $$ \begin{align} U\ket{0}^{\lceil\log_2 N\rceil}\ket{0}^{m}=\sum_{j=0}^{N-1}\sqrt{p_j} \ket{j}\ket{\text{garbage}_j}.</span></span>
<span data-ttu-id="5366a-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="5366a-111">\end{align} $$</span></span>

```qsharp
function QuantumROM (targetError : Double, coefficients : Double[]) : ((Int, (Int, Int)), Double, ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))
```


## <a name="input"></a><span data-ttu-id="5366a-112">입력</span><span class="sxs-lookup"><span data-stu-id="5366a-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="5366a-113">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5366a-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5366a-114">$ \Epsilon $ 대상 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="5366a-115">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="5366a-115">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="5366a-116">기본 상태의 확률을 지정 하는 $N $ 계수의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-116">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="5366a-117">음수 $-\ alpha_j $는 긍정 $ | \ alpha_j | $로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--intintintdoublelittleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="5366a-118">Output: (([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double), ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Adj []](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is + Ctl)</span><span class="sxs-lookup"><span data-stu-id="5366a-118">Output : (([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))),[Double](xref:microsoft.quantum.lang-ref.double),([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

## <a name="first-parameter"></a><span data-ttu-id="5366a-119">첫 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5366a-119">First parameter</span></span>

<span data-ttu-id="5366a-120">`(x,(y,z))`는 할당 된 총 수 인 튜플을,는 레지스터의 값이 고,은 `x = y + z` `y` 가비지 비트 수입니다 `LittleEndian` `z` .</span><span class="sxs-lookup"><span data-stu-id="5366a-120">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>

## <a name="second-parameter"></a><span data-ttu-id="5366a-121">두 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5366a-121">Second parameter</span></span>

<span data-ttu-id="5366a-122">계수 배열의 일회용 $ \ sum_j | \ alpha_j | $입니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-122">The one-norm $\sum_j |\alpha_j|$ of the coefficient array.</span></span>

## <a name="third-parameter"></a><span data-ttu-id="5366a-123">세 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5366a-123">Third parameter</span></span>

<span data-ttu-id="5366a-124">단일 $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="5366a-124">The unitary $U$.</span></span>

## <a name="references"></a><span data-ttu-id="5366a-125">참조 항목</span><span class="sxs-lookup"><span data-stu-id="5366a-125">References</span></span>

- <span data-ttu-id="5366a-126">선형 T 복잡성 Ryan Babbush, Craig Gidney, Dominic Berry, 네, Spectra Wiebe, Jarrod McClean, Alexandru 고, 연한, 오스틴 Fowler, Hartmut Neven를 사용 하 여 퀀텀 회로에서 전자 인코딩 https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="5366a-126">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>