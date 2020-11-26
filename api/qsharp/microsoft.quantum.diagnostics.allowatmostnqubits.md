---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: AllowAtMostNQubits 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 5376b6f39d12d664342fbf71e67442c6ef8a0827
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202552"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="807a8-102">AllowAtMostNQubits 작업</span><span class="sxs-lookup"><span data-stu-id="807a8-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="807a8-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="807a8-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="807a8-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="807a8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="807a8-105">이 작업과 adjoint 호출 사이에는 지정 된 수의 추가 비트 수를 사용 하 여 문을 사용 하 여 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="807a8-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="807a8-106">입력</span><span class="sxs-lookup"><span data-stu-id="807a8-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="807a8-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="807a8-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="807a8-108">할당할 수 있는 최대 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="807a8-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="807a8-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="807a8-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="807a8-110">실패 시 표시 되는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="807a8-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="807a8-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="807a8-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="807a8-112">설명</span><span class="sxs-lookup"><span data-stu-id="807a8-112">Remarks</span></span>

<span data-ttu-id="807a8-113">이 작업을 지원 하지 않는 대상에서는이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="807a8-113">This operation may be replaced by a no-op on targets which do not support it.</span></span>