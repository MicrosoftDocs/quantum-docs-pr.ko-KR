---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: SelectZ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 171bbe28ce8f10ca4b213a94b23f8c049546e3bf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713791"
---
# <a name="selectz-operation"></a><span data-ttu-id="b2b5a-102">SelectZ 작업</span><span class="sxs-lookup"><span data-stu-id="b2b5a-102">SelectZ operation</span></span>

<span data-ttu-id="b2b5a-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="b2b5a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="b2b5a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b2b5a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b2b5a-105">인덱스 상태 $ \ket{p} $에서 $ 조건 화 된에 대 한 $Z $ $p gate를 적용 하는 단일 $U $입니다.</span><span class="sxs-lookup"><span data-stu-id="b2b5a-105">A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$.</span></span> <span data-ttu-id="b2b5a-106">즉, $ $ \begin{align} U\ket {p} \ k {\ psi} = \ket{p}Z \_ p\ket {\ psi} \end{align} $ $입니다.</span><span class="sxs-lookup"><span data-stu-id="b2b5a-106">That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$</span></span>

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b2b5a-107">입력</span><span class="sxs-lookup"><span data-stu-id="b2b5a-107">Input</span></span>

### <a name="indexregister--littleendian"></a><span data-ttu-id="b2b5a-108">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b2b5a-108">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b2b5a-109">이 레지스터의 $ \ket{p} $ 상태에 따라 $가 적용 되는가 $Z 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2b5a-109">The state $\ket{p}$ of this register determines the qubit on which $Z$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="b2b5a-110">targetRegister: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b2b5a-110">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2b5a-111">Pauli 연산자가 적용 되는 원하는 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="b2b5a-111">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b2b5a-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2b5a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

