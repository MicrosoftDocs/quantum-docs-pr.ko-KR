---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: ApplyPauli 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: ccf8e1b3dbe5d4cd916a581aeab190ab0cff2021
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717816"
---
# <a name="applypauli-operation"></a><span data-ttu-id="d37b4-102">ApplyPauli 작업</span><span class="sxs-lookup"><span data-stu-id="d37b4-102">ApplyPauli operation</span></span>

<span data-ttu-id="d37b4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d37b4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d37b4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d37b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d37b4-105">여러 기능을 제공 하는 경우 해당 작업을 레지스터에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37b4-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d37b4-106">입력</span><span class="sxs-lookup"><span data-stu-id="d37b4-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="d37b4-107">pauli: [pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="d37b4-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="d37b4-108">단일 수준 비트 Pauli 연산자의 배열로 표현 되는 다중 기능 비트 Pauli 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="d37b4-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d37b4-109">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d37b4-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d37b4-110">등록 하 여 지정 된 Pauli 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37b4-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d37b4-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d37b4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

