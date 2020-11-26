---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: EncodeIntoBitFlipCode 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: b27759caba3c5dd363dbdf24d6e5de76870173cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200954"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="d4ff0-102">EncodeIntoBitFlipCode 작업</span><span class="sxs-lookup"><span data-stu-id="d4ff0-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="d4ff0-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d4ff0-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d4ff0-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d4ff0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d4ff0-105">[3, 1, 3]/⟦ 3, 1, 1 ⟧ 비트 대칭 코드를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="d4ff0-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="d4ff0-106">입력</span><span class="sxs-lookup"><span data-stu-id="d4ff0-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="d4ff0-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4ff0-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d4ff0-108">보호할 데이터를 나타내는 실제 및 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="d4ff0-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="d4ff0-109">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4ff0-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d4ff0-110">{00}보호할 데이터를 인코딩하는 데 사용 되는 처음에 $ \ket $ 상태에 있는 보조 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="d4ff0-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="d4ff0-111">출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="d4ff0-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="d4ff0-112">인코딩에 사용 되는 실제 및 보조 비트 (논리적 레지스터로 나타냄)입니다.</span><span class="sxs-lookup"><span data-stu-id="d4ff0-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4ff0-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d4ff0-113">See Also</span></span>

- [<span data-ttu-id="d4ff0-114">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="d4ff0-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)