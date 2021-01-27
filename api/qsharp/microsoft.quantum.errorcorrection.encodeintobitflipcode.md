---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: EncodeIntoBitFlipCode 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 44034a864c946a7d3dbb21bad5ee500660709f1a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826671"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="58950-102">EncodeIntoBitFlipCode 작업</span><span class="sxs-lookup"><span data-stu-id="58950-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="58950-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="58950-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="58950-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="58950-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="58950-105">[3, 1, 3]/⟦ 3, 1, 1 ⟧ 비트 대칭 코드를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="58950-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="58950-106">입력</span><span class="sxs-lookup"><span data-stu-id="58950-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="58950-107">physRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="58950-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="58950-108">보호할 데이터를 나타내는 실제 및 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="58950-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="58950-109">auxQubits: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="58950-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="58950-110">{00}보호할 데이터를 인코딩하는 데 사용 되는 처음에 $ \ket $ 상태에 있는 보조 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="58950-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="58950-111">출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="58950-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="58950-112">인코딩에 사용 되는 실제 및 보조 비트 (논리적 레지스터로 나타냄)입니다.</span><span class="sxs-lookup"><span data-stu-id="58950-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="58950-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="58950-113">See Also</span></span>

- [<span data-ttu-id="58950-114">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="58950-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)