---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: PrepareSingleQubitIdentity 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: 12a650568aa5682e8fb6498808d188b154527acb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724883"
---
# <a name="preparesinglequbitidentity-operation"></a><span data-ttu-id="dd3e1-102">PrepareSingleQubitIdentity 작업</span><span class="sxs-lookup"><span data-stu-id="dd3e1-102">PrepareSingleQubitIdentity operation</span></span>

<span data-ttu-id="dd3e1-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="dd3e1-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="dd3e1-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dd3e1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dd3e1-105">최대 혼합 상태에서 고 비트를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd3e1-105">Prepares a qubit in the maximally mixed state.</span></span>

<span data-ttu-id="dd3e1-106">Depolarizing channel $ $ \begin{align} \00P (\rho) \mathrel{를 적용 하 여 $ \boldone/$2 상태에서 지정 된 비트를 준비 합니다. =} \frac {1} {4} \ sum_ {\omega \omega \{ 0, 1, 2, 3 \} } \omega \_ {\mu} \rho \omega \_ {\mu} ^ {\dagger}, \end{align} $ $ where $ \omega \_ i $는 $i $ th pauli 연산자 이며 여기서 $ \rho $는 혼합 상태를 나타내는 밀도 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="dd3e1-106">It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.</span></span>

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="dd3e1-107">입력</span><span class="sxs-lookup"><span data-stu-id="dd3e1-107">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="dd3e1-108">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dd3e1-108">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dd3e1-109">위에서 설명한 방식으로 상태가 depolarized 인 이상 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="dd3e1-109">A qubit whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dd3e1-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dd3e1-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dd3e1-111">설명</span><span class="sxs-lookup"><span data-stu-id="dd3e1-111">Remarks</span></span>

<span data-ttu-id="dd3e1-112">상태에이 작업을 적용 한 결과를 설명 하는 혼합 상태 $ \boldone/$2는이 작업에서 수행 되는 임의의 선택 항목에 대 한 예상 값을 암시적으로 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd3e1-112">The mixed state $\boldone / 2$ describing the result of applying this operation to a state implicitly describes an expectation value over random choices made in this operation.</span></span>
<span data-ttu-id="dd3e1-113">따라서 단일 응용 프로그램의 경우이 작업은 순수 상태를 순수 상태에 매핑하고 기대에 설명 된 대로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd3e1-113">Thus, for any single application, this operation maps pure states to pure states, but it acts as described in expectation.</span></span>
<span data-ttu-id="dd3e1-114">특히이 작업은 process tomography에서 사용 하 여 채널의 *비 unital* 구성 요소를 측정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd3e1-114">In particular, this operation can be used in process tomography to measure the *non-unital* components of a channel.</span></span>