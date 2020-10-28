---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: AssertAllZeroWithinTolerance 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 5e401904086323fabef7914d34463f50e4c38862
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713042"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="0bb3b-102">AssertAllZeroWithinTolerance 작업</span><span class="sxs-lookup"><span data-stu-id="0bb3b-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="0bb3b-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="0bb3b-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="0bb3b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0bb3b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0bb3b-105">지정 된 것과 같은 Assert는 {0} 지정 된 허용 오차까지 모두 $ \ket $ 상태에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3b-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="0bb3b-106">입력</span><span class="sxs-lookup"><span data-stu-id="0bb3b-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="0bb3b-107">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0bb3b-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0bb3b-108">$ \Ket $ 상태에 있도록 어설션된 비트입니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="0bb3b-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="0bb3b-109">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0bb3b-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0bb3b-110">상태가 $ \ket $ 상태 여야 하는 정확도 {0}</span><span class="sxs-lookup"><span data-stu-id="0bb3b-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="0bb3b-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0bb3b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0bb3b-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0bb3b-112">See Also</span></span>

- [<span data-ttu-id="0bb3b-113">AssertQubitWithinTolerance.</span><span class="sxs-lookup"><span data-stu-id="0bb3b-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)