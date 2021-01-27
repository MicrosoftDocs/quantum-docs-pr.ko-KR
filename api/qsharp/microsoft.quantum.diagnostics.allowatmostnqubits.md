---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: AllowAtMostNQubits 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 3aa80767ac0f752e7be0efa2966c580ca3cb8f19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830907"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="76c09-102">AllowAtMostNQubits 작업</span><span class="sxs-lookup"><span data-stu-id="76c09-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="76c09-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="76c09-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="76c09-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="76c09-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="76c09-105">이 작업과 adjoint 호출 사이에는 지정 된 수의 추가 비트 수를 사용 하 여 문을 사용 하 여 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c09-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="76c09-106">입력</span><span class="sxs-lookup"><span data-stu-id="76c09-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="76c09-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="76c09-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="76c09-108">할당할 수 있는 최대 비트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="76c09-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="76c09-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="76c09-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="76c09-110">실패 시 표시 되는 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="76c09-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="76c09-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76c09-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="76c09-112">예</span><span class="sxs-lookup"><span data-stu-id="76c09-112">Example</span></span>

<span data-ttu-id="76c09-113">다음 코드 조각은이 진단을 지 원하는 컴퓨터에서 실행 되는 경우 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c09-113">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
within {
    AllowAtMostNQubits(3, "Too many qubits allocated.");
} apply {
    // Fails since this allocates four qubits.
    using (register = Qubit[4]) {
    }
}
```

## <a name="remarks"></a><span data-ttu-id="76c09-114">설명</span><span class="sxs-lookup"><span data-stu-id="76c09-114">Remarks</span></span>

<span data-ttu-id="76c09-115">이 작업을 지원 하지 않는 대상에서는이 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="76c09-115">This operation may be replaced by a no-op on targets which do not support it.</span></span>