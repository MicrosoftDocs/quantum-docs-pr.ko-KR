---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: ObliviousOracle 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 793e72af56e288f9b437302f9958665e92e5e763
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842557"
---
# <a name="obliviousoracle-user-defined-type"></a><span data-ttu-id="00090-102">ObliviousOracle 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="00090-102">ObliviousOracle user defined type</span></span>

<span data-ttu-id="00090-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="00090-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="00090-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="00090-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="00090-105">명확한 진폭 증폭의 oracle을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00090-105">Represents an oracle for oblivious amplitude amplification.</span></span>

<span data-ttu-id="00090-106">Oracle $O $에 대 한 입력은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00090-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="00090-107">$O $가 작동 하는 ancilla 레지스터 $a $입니다.</span><span class="sxs-lookup"><span data-stu-id="00090-107">The ancilla register $a$ that $O$ acts on.</span></span>
- <span data-ttu-id="00090-108">원하는 단일 $U $이 적용 되 고, $ \ket{t} a $ 상태에 있는 레지스터 $a $에서 게시 된 시스템 등록 $s $입니다 \_ .</span><span class="sxs-lookup"><span data-stu-id="00090-108">The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.</span></span>

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="00090-109">설명</span><span class="sxs-lookup"><span data-stu-id="00090-109">Remarks</span></span>

<span data-ttu-id="00090-110">$ $ O\ket {s} \_ a\ket {\ psi} \_ s = \Lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} a\cdots $ $에 의해 정의 된이 oracle은 \_ ancilla state $ \ket{s} \_ a $U $에 적용 되어 모든 시스템 상태 $ \ket{\psi} \_ s $ with 진폭 $ \lambda $를 사용 하 여 $ \ket{t} \_ a $로 플래그 지정 된 모든 시스템 상태 $</span><span class="sxs-lookup"><span data-stu-id="00090-110">This oracle defined by $$ O\ket{s}\_a\ket{\psi}\_s= \lambda\ket{t}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{t^\perp}\_a\cdots $$ acts on the ancilla state $\ket{s}\_a$ to implement the unitary $U$ on any system state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{t}\_a$.</span></span>
<span data-ttu-id="00090-111">첫 번째 매개 변수는 $ \ket{s} a $의 기본 비트 레지스터입니다 \_ .</span><span class="sxs-lookup"><span data-stu-id="00090-111">The first parameter is the qubit register of $\ket{s}\_a$.</span></span> <span data-ttu-id="00090-112">두 번째 매개 변수는 $ \ket{\psi} s $의 고 비트 레지스터입니다 \_ .</span><span class="sxs-lookup"><span data-stu-id="00090-112">The second parameter is the qubit register of $\ket{\psi}\_s$.</span></span>