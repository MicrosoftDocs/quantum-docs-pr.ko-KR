---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: AllowAtMostNQubits 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: ddbed96df0d95cfd78730c091a6a81ee6e49c349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713056"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="40e1f-102">AllowAtMostNQubits 작업</span><span class="sxs-lookup"><span data-stu-id="40e1f-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="40e1f-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="40e1f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="40e1f-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40e1f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40e1f-105">이 작업과 adjoint 호출 사이에는 지정 된 수의 추가 비트 수를 사용 하 여 문을 사용 하 여 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="40e1f-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="40e1f-106">입력</span><span class="sxs-lookup"><span data-stu-id="40e1f-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="40e1f-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40e1f-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="40e1f-108">할당할 수 있는 최대 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="40e1f-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="40e1f-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="40e1f-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="40e1f-110">실패 시 표시 되는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="40e1f-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="40e1f-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="40e1f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="40e1f-112">설명</span><span class="sxs-lookup"><span data-stu-id="40e1f-112">Remarks</span></span>

<span data-ttu-id="40e1f-113">이 작업을 지원 하지 않는 대상에서는이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="40e1f-113">This operation may be replaced by a no-op on targets which do not support it.</span></span>