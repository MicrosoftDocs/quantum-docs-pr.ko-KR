---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: EncodeIntoBitFlipCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 694d3f7a412b64b0ad533b4478a9274384d05c61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712405"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="16862-102">EncodeIntoBitFlipCode 작업</span><span class="sxs-lookup"><span data-stu-id="16862-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="16862-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="16862-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="16862-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="16862-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="16862-105">[3, 1, 3]/⟦ 3, 1, 1 ⟧ 비트 대칭 코드를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="16862-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="16862-106">입력</span><span class="sxs-lookup"><span data-stu-id="16862-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="16862-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="16862-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="16862-108">보호할 데이터를 나타내는 실제 및 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="16862-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="16862-109">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="16862-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="16862-110">{00}보호할 데이터를 인코딩하는 데 사용 되는 처음에 $ \ket $ 상태에 있는 보조 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="16862-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="16862-111">출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="16862-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="16862-112">인코딩에 사용 되는 실제 및 보조 비트 (논리적 레지스터로 나타냄)입니다.</span><span class="sxs-lookup"><span data-stu-id="16862-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="16862-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="16862-113">See Also</span></span>

- [<span data-ttu-id="16862-114">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="16862-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)