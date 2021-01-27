---
uid: Microsoft.Quantum.Intrinsic.Reset
title: 작업 다시 설정
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: b4275796b966bfe7f55271f4e92866410a14e830
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818637"
---
# <a name="reset-operation"></a><span data-ttu-id="0cb2b-102">작업 다시 설정</span><span class="sxs-lookup"><span data-stu-id="0cb2b-102">Reset operation</span></span>

<span data-ttu-id="0cb2b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="0cb2b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="0cb2b-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0cb2b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="0cb2b-105">단일의 비트를 고려 하 여이를 측정 하 고 안전 하 게 해제할 수 있도록 | 0 ⟩ 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cb2b-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="0cb2b-106">입력</span><span class="sxs-lookup"><span data-stu-id="0cb2b-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="0cb2b-107">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0cb2b-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0cb2b-108">상태를 $ \ket $로 다시 설정 해야 하는 이상 비트입니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="0cb2b-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0cb2b-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0cb2b-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

