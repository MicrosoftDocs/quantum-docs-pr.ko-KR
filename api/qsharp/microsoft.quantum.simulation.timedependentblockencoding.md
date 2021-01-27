---
uid: Microsoft.Quantum.Simulation.TimeDependentBlockEncoding
title: TimeDependentBlockEncoding 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentBlockEncoding
qsharp.summary: >-
  Represents a `BlockEncoding` that is controlled by a clock register.

  That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k. \end{align} $$.
ms.openlocfilehash: e2b191a4fc44f99c88f25da9b1ee6460d936740b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814275"
---
# <a name="timedependentblockencoding-user-defined-type"></a><span data-ttu-id="b2b75-102">TimeDependentBlockEncoding 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="b2b75-102">TimeDependentBlockEncoding user defined type</span></span>

<span data-ttu-id="b2b75-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b2b75-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b2b75-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b2b75-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b2b75-105">클록 레지스터에 의해 제어 되는를 나타냅니다 `BlockEncoding` .</span><span class="sxs-lookup"><span data-stu-id="b2b75-105">Represents a `BlockEncoding` that is controlled by a clock register.</span></span>

<span data-ttu-id="b2b75-106">즉,는 `TimeDependentBlockEncoding` 클록 등록 시 $ \ket{k} _d $ 상태에 의해 제어 되는 단일 $U $로, `d` 시스템 레지스터에 대해 작동 하는 임의 연산자 $H _k $에 해당 하는 `s` 것이 보조 상태 $ \ket _a $에 해당 하는 왼쪽 위의 블록으로 인코딩됩니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="b2b75-106">That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="b2b75-107">즉, 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b2b75-107">That is,</span></span>

<span data-ttu-id="b2b75-108">$ $ \begin{align} (\bra {0} \_ a\otimes I_ {ds}) U (\ket {0} \_ a\otimes I_ {ds}) = \ sum_ {k} \ket{k}\bra{k} \_ d\otimes H_k.</span><span class="sxs-lookup"><span data-stu-id="b2b75-108">$$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k.</span></span>
<span data-ttu-id="b2b75-109">\end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="b2b75-109">\end{align} $$.</span></span>

```qsharp

newtype TimeDependentBlockEncoding = (((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

