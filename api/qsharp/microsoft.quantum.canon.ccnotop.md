---
uid: Microsoft.Quantum.Canon.CCNOTop
title: CCNOTop 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CCNOTop
qsharp.summary: The signature type of CCNOT gate.
ms.openlocfilehash: 533ea87e137aabf6f75e6096dc710ca15c984f25
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207482"
---
# <a name="ccnotop-user-defined-type"></a><span data-ttu-id="75d75-102">CCNOTop 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="75d75-102">CCNOTop user defined type</span></span>

<span data-ttu-id="75d75-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="75d75-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="75d75-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="75d75-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="75d75-105">CCNOT gate의 서명 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="75d75-105">The signature type of CCNOT gate.</span></span>

```qsharp

newtype CCNOTop = (Apply : ((Qubit, Qubit, Qubit) => Unit is Adj));
```



## <a name="named-items"></a><span data-ttu-id="75d75-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="75d75-106">Named Items</span></span>

### <a name="apply--qubitqubitqubit--unit--is-adj"></a><span data-ttu-id="75d75-107">Apply[: (Adj bit,](xref:microsoft.quantum.lang-ref.qubit) [bit](xref:microsoft.quantum.lang-ref.qubit), [bit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is</span><span class="sxs-lookup"><span data-stu-id="75d75-107">Apply : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

