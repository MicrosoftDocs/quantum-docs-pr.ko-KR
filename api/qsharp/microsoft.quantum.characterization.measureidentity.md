---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: MeasureIdentity 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 4a169355d0669c67f0eb14c80e8554b2f24b035a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216118"
---
# <a name="measureidentity-operation"></a><span data-ttu-id="a1366-102">MeasureIdentity 작업</span><span class="sxs-lookup"><span data-stu-id="a1366-102">MeasureIdentity operation</span></span>

<span data-ttu-id="a1366-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="a1366-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="a1366-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a1366-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a1366-105">은 (는) 다양 한 비트의 레지스터에서 identity 연산자를 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1366-105">Measures the identity operator on a register of qubits.</span></span>

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="a1366-106">입력</span><span class="sxs-lookup"><span data-stu-id="a1366-106">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="a1366-107">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a1366-107">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a1366-108">측정할 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="a1366-108">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a1366-109">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="a1366-109">Output : __invalid<Result>__</span></span>

<span data-ttu-id="a1366-110">결과 값 `Zero` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a1366-110">The result value `Zero`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1366-111">설명</span><span class="sxs-lookup"><span data-stu-id="a1366-111">Remarks</span></span>

<span data-ttu-id="a1366-112">$ \Boldone $에는 eigenvalue $1 $만 있고 음수 eigenvalue이 없기 때문에이 작업은 항상를 반환 하며 `Zero` ,이는 eigenvalue $ + 1 = (-1) ^ 0 $에 해당 하며, 상태를 축소 하지 않습니다 `register` .</span><span class="sxs-lookup"><span data-stu-id="a1366-112">Since $\boldone$ has only the eigenvalue $1$, and does not have a negative eigenvalue, this operation always returns `Zero`, corresponding to the eigenvalue $+1 = (-1)^0$, and does not cause a collapse of the state of `register`.</span></span>

<span data-ttu-id="a1366-113">자체적으로이 작업은 유용 하지 않지만 프로세스 tomography의 컨텍스트에서는 퀀텀 프로세스의 추적 유지에 대 한 정보를 제공 하므로 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1366-113">On its own, this operation is not useful, but is helpful in the context of process tomography, as it provides information about the trace preservation of a quantum process.</span></span>
<span data-ttu-id="a1366-114">특히 손실 측정이 있는 대상 컴퓨터는 $ \boldone $의 실제 측정을 통해이 작업을 대체 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1366-114">In particular, a target machine with lossy measurement should replace this operation by an actual measurement of $\boldone$.</span></span>