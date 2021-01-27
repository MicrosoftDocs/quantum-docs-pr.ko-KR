---
uid: Microsoft.Quantum.Oracles.StateOracle
title: StateOracle 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 005d7862214abb3dcb9c0caa006343720d179a52
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854478"
---
# <a name="stateoracle-user-defined-type"></a><span data-ttu-id="76da5-102">StateOracle 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="76da5-102">StateOracle user defined type</span></span>

<span data-ttu-id="76da5-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="76da5-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="76da5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="76da5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="76da5-105">상태 준비를 위한 oracle을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76da5-105">Represents an oracle for state preparation.</span></span>

<span data-ttu-id="76da5-106">Oracle $O $에 대 한 입력은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76da5-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="76da5-107">플래그 $f $를 인덱싱하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="76da5-107">An integer indexing the flag qubit $f$.</span></span>
- <span data-ttu-id="76da5-108">필요한 퀀텀 상태 $ \ket{\psi} s $를 저장할 시스템 등록 $s $ \_ 입니다.</span><span class="sxs-lookup"><span data-stu-id="76da5-108">The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="76da5-109">설명</span><span class="sxs-lookup"><span data-stu-id="76da5-109">Remarks</span></span>

<span data-ttu-id="76da5-110">$ $ O\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, $ $에서 정의한이 oracle은 계산 기준 상태 $ \ket {f} \ket s $에 대해 작동 하 여 $ \ket{\psi} {0} \_ {0} \_ \_ {1} f $로 플래그가 지정 된 기준으로 대상 상태 $ \ket s $를 만듭니다 \_ .</span><span class="sxs-lookup"><span data-stu-id="76da5-110">This oracle defined by $$ O\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, $$ acts on the on computational basis state $\ket{0}\_{f}\ket{0}\_s$ to create the target state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{1}\_f$.</span></span>
<span data-ttu-id="76da5-111">첫 번째 매개 변수는 $ \ket f $의 고 비트 레지스터에 대 한 인덱스입니다 {0} \_ .</span><span class="sxs-lookup"><span data-stu-id="76da5-111">The first parameter is an index to the qubit register of $\ket{0}\_f$.</span></span> <span data-ttu-id="76da5-112">두 번째 매개 변수는 두 레지스터를 모두 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="76da5-112">The second parameter encompassed both registers.</span></span>