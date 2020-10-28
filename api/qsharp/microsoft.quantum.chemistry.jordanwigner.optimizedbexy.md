---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEXY
title: OptimizedBEXY 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEXY
qsharp.summary: A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$. That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$
ms.openlocfilehash: 359d347fc57be46200a218646911a7a400b4a96d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713910"
---
# <a name="optimizedbexy-operation"></a><span data-ttu-id="a1dcc-102">OptimizedBEXY 작업</span><span class="sxs-lookup"><span data-stu-id="a1dcc-102">OptimizedBEXY operation</span></span>

<span data-ttu-id="a1dcc-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="a1dcc-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="a1dcc-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a1dcc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a1dcc-105">$ (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1}에 pauli 문자열을 적용 하는 단일 $U $ 인덱스에서 $ on stbits $0 조건 화 된 p $를 Z_0 합니다 $z \in \{ 0, 1 \} $ 및 $p $입니다.</span><span class="sxs-lookup"><span data-stu-id="a1dcc-105">A unitary $U$ that applies the Pauli string on $(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0$ on qubits $0..p$ conditioned on an index $z\in\{0,1\}$ and $p$.</span></span> <span data-ttu-id="a1dcc-106">즉, $ $ \begin{align} U\ket {z} \ k {p} \ k {\ psi} = \ket{z}\ket{p} (X ^ {z + 1} \_ pY ^ {z} \_ p) z \_ {p-1} ... Z_0 \ket{\psi} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="a1dcc-106">That is, $$ \begin{align} U\ket{z}\ket{p}\ket{\psi} = \ket{z}\ket{p}(X^{z+1}\_pY^{z}\_p)Z\_{p-1}...Z_0\ket{\psi} \end{align} $$</span></span>

```qsharp
operation OptimizedBEXY (pauliBasis : Qubit, indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="a1dcc-107">입력</span><span class="sxs-lookup"><span data-stu-id="a1dcc-107">Input</span></span>

### <a name="paulibasis--qubit"></a><span data-ttu-id="a1dcc-108">pauliBasis: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a1dcc-108">pauliBasis : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a1dcc-109">이 고가 $ \ket $ 상태에 있는 경우 {0} $X $가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1dcc-109">When this qubit is in state $\ket{0}$, $X$ is applied.</span></span> <span data-ttu-id="a1dcc-110">상태가 $ \ket $ 인 경우 {1} $Y $가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1dcc-110">When it is in state $\ket{1}$, $Y$ is applied.</span></span>


### <a name="indexregister--littleendian"></a><span data-ttu-id="a1dcc-111">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a1dcc-111">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a1dcc-112">이 레지스터의 $ \ket{p} $ 상태에 따라 $ 또는 $Y $가 적용 되는가 $X 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1dcc-112">The state $\ket{p}$ of this register determines the qubit on which $X$ or $Y$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="a1dcc-113">targetRegister: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a1dcc-113">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a1dcc-114">Pauli 연산자가 적용 되는 원하는 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="a1dcc-114">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a1dcc-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a1dcc-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="a1dcc-116">참조</span><span class="sxs-lookup"><span data-stu-id="a1dcc-116">References</span></span>

- <span data-ttu-id="a1dcc-117">선형 T 복잡성 Ryan Babbush, Craig Gidney, Dominic Berry, 네, Spectra Wiebe, Jarrod McClean, Alexandru 고, 연한, 오스틴 Fowler, Hartmut Neven를 사용 하 여 퀀텀 회로에서 전자 인코딩 https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="a1dcc-117">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>