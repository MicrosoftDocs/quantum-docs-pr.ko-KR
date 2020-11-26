---
uid: Microsoft.Quantum.Intrinsic.Reset
title: 작업 다시 설정
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: 61b5e4ccdf009dcb6c639e3d8e23bc73a6e475b5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198676"
---
# <a name="reset-operation"></a><span data-ttu-id="1479d-102">작업 다시 설정</span><span class="sxs-lookup"><span data-stu-id="1479d-102">Reset operation</span></span>

<span data-ttu-id="1479d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="1479d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="1479d-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1479d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1479d-105">단일의 비트를 고려 하 여이를 측정 하 고 안전 하 게 해제할 수 있도록 | 0 ⟩ 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1479d-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="1479d-106">입력</span><span class="sxs-lookup"><span data-stu-id="1479d-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="1479d-107">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1479d-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1479d-108">상태를 $ \ket $로 다시 설정 해야 하는 이상 비트입니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="1479d-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1479d-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1479d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

