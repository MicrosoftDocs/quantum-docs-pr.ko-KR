---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: BlockEncoding 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 75fdbf13cf07d906982d4a611d1d25b3e29db2cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225434"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="7bfa2-102">BlockEncoding 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="7bfa2-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="7bfa2-103">네임 스페이스: [Microsoft 양자 시뮬레이션](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7bfa2-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7bfa2-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7bfa2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7bfa2-105">관심이 있는 임의의 연산자가 왼쪽 위 블록에서 인코딩된 단일를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7bfa2-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="7bfa2-106">즉,는 `BlockEncoding` 시스템 레지스터에 대해 수행 되는 임의의 연산자 $H $ `s` \ket _a $에 해당 하는 왼쪽 위 블록에 인코딩 되는 임의의 연산자를 갖는 단일 $U $ {0} 입니다.</span><span class="sxs-lookup"><span data-stu-id="7bfa2-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="7bfa2-107">즉, 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7bfa2-107">That is,</span></span>

<span data-ttu-id="7bfa2-108">$ $ \begin{align} (\bra {0} _a \otimes I_s) U (\ket {0} _a \otimes I_s) = H \end{align} $ $.</span><span class="sxs-lookup"><span data-stu-id="7bfa2-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

