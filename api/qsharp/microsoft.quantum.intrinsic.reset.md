---
uid: Microsoft.Quantum.Intrinsic.Reset
title: 작업 다시 설정
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: c89cbbce49e294e56abc11b3b0492d2ed8e980a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720872"
---
# <a name="reset-operation"></a><span data-ttu-id="e33a4-102">작업 다시 설정</span><span class="sxs-lookup"><span data-stu-id="e33a4-102">Reset operation</span></span>

<span data-ttu-id="e33a4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="e33a4-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="e33a4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e33a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e33a4-105">단일의 비트를 고려 하 여이를 측정 하 고 안전 하 게 해제할 수 있도록 | 0 ⟩ 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e33a4-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="e33a4-106">입력</span><span class="sxs-lookup"><span data-stu-id="e33a4-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="e33a4-107">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e33a4-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e33a4-108">상태를 $ \ket $로 다시 설정 해야 하는 이상 비트입니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="e33a4-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e33a4-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e33a4-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

