---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: PrepareChoiState 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: ced71c4278f42f577760acd54ae53e7f5e6dae4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210576"
---
# <a name="preparechoistate-operation"></a><span data-ttu-id="b2083-102">PrepareChoiState 작업</span><span class="sxs-lookup"><span data-stu-id="b2083-102">PrepareChoiState operation</span></span>

<span data-ttu-id="b2083-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b2083-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b2083-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b2083-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b2083-105">지정 된 작업에 대 한 Choi – Jamiołkowski 상태를 지정 된 참조 및 대상 레지스터로 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2083-105">Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b2083-106">입력</span><span class="sxs-lookup"><span data-stu-id="b2083-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="b2083-107">op:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[] => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2083-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="b2083-108">작업 $ \Lambda $ Choi – Jamiołkowski state $J (\Lambda)/2 ^ N $를 준비할 수 있습니다. 여기서 $N $은가 작동 하는가 중 비트 수입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="b2083-108">Operation $\Lambda$ whose Choi–Jamiołkowski state $J(\Lambda) / 2^N$ is to be prepared, where $N$ is the number of qubits on which `op` acts.</span></span>


### <a name="reference--qubit"></a><span data-ttu-id="b2083-109">참조:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b2083-109">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2083-110">의 동작에 대 한 참조로 사용 되는 $ \ket{00\cdots 0} $ 상태에서 시작 하는 비트의 레지스터입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="b2083-110">A register of qubits starting in the $\ket{00\cdots 0}$ state to be used as a reference for the action of `op`.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b2083-111">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b2083-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2083-112">처음에이 적용 될 $ \ket{00\cdots 0} $ 상태에 있는 나머지 비트의 레지스터입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="b2083-112">A register of qubits initially in the $\ket{00\cdots 0}$ state on which `op` is to be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b2083-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2083-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b2083-114">설명</span><span class="sxs-lookup"><span data-stu-id="b2083-114">Remarks</span></span>

<span data-ttu-id="b2083-115">퀀텀 프로세스의 Choi – Jamiłkowski state $J (\Lambda) $는 $ $ \begin{align} J (\Lambda) \mathrel{: =} (\boldone \otimes \Lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ where $ |로 정의 됩니다. X\rangle \! \rangle $는 열 스택 규칙에서 행렬 $X $의 *벡터화* 입니다.</span><span class="sxs-lookup"><span data-stu-id="b2083-115">The Choi–Jamiłkowski state $J(\Lambda)$ of a quantum process is defined as $$ \begin{align} J(\Lambda) \mathrel{:=} (\boldone \otimes \Lambda) (|\boldone\rangle\!\rangle\langle\!\langle\boldone|), \end{align} $$ where $|X\rangle\!\rangle$ is the *vectorization* of a matrix $X$ in the column-stacking convention.</span></span> <span data-ttu-id="b2083-116">이 상태에 대 한 기존 설명 학습은 임의의 입력 상태에서 수행 되는 $ \Lambda $의 효과에 대 한 전체 정보를 제공 하 고, *퀀텀 프로세스 tomography* 의 토대를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2083-116">Learning a classical description of this state provides full information about the effect of $\Lambda$ acting on arbitrary input states, and forms the foundation of *quantum process tomography*.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2083-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b2083-117">See Also</span></span>

- [<span data-ttu-id="b2083-118">PrepareChoiStateA.</span><span class="sxs-lookup"><span data-stu-id="b2083-118">Microsoft.Quantum.Preparation.PrepareChoiStateA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [<span data-ttu-id="b2083-119">PrepareChoiStateC.</span><span class="sxs-lookup"><span data-stu-id="b2083-119">Microsoft.Quantum.Preparation.PrepareChoiStateC</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [<span data-ttu-id="b2083-120">PrepareChoiStateCA.</span><span class="sxs-lookup"><span data-stu-id="b2083-120">Microsoft.Quantum.Preparation.PrepareChoiStateCA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)