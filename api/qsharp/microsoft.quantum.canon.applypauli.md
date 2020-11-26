---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: ApplyPauli 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: 7f42d9cab2f80f8f826ad1268b050134f0540cdd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218226"
---
# <a name="applypauli-operation"></a><span data-ttu-id="a2218-102">ApplyPauli 작업</span><span class="sxs-lookup"><span data-stu-id="a2218-102">ApplyPauli operation</span></span>

<span data-ttu-id="a2218-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a2218-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a2218-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2218-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a2218-105">여러 기능을 제공 하는 경우 해당 작업을 레지스터에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2218-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a2218-106">입력</span><span class="sxs-lookup"><span data-stu-id="a2218-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="a2218-107">pauli: [pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="a2218-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="a2218-108">단일 수준 비트 Pauli 연산자의 배열로 표현 되는 다중 기능 비트 Pauli 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="a2218-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="a2218-109">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a2218-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a2218-110">등록 하 여 지정 된 Pauli 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2218-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a2218-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a2218-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

