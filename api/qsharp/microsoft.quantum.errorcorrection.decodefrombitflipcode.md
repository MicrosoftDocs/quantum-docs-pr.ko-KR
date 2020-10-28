---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: DecodeFromBitFlipCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: be6ad5fce9eeb3eea031ff301b78dbb3680b66f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712482"
---
# <a name="decodefrombitflipcode-operation"></a><span data-ttu-id="bedac-102">DecodeFromBitFlipCode 작업</span><span class="sxs-lookup"><span data-stu-id="bedac-102">DecodeFromBitFlipCode operation</span></span>

<span data-ttu-id="bedac-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="bedac-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="bedac-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bedac-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bedac-105">[3, 1, 3]/⟦ 3, 1, 1 ⟧ 비트 대칭 코드에서 디코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="bedac-105">Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="bedac-106">입력</span><span class="sxs-lookup"><span data-stu-id="bedac-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="bedac-107">logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="bedac-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="bedac-108">비트 대칭 코드의 코드 블록입니다.</span><span class="sxs-lookup"><span data-stu-id="bedac-108">A code block of the bit-flip code.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="bedac-109">Output[: ((),](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)])</span><span class="sxs-lookup"><span data-stu-id="bedac-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="bedac-110">논리적 레지스터로 인코딩된 데이터의 튜플 및 증후군를 나타내는 데 사용 되는 보조 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="bedac-110">A tuple of the data encoded into the logical register, and the auxiliary qubits used to represent the syndrome.</span></span>

## <a name="see-also"></a><span data-ttu-id="bedac-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bedac-111">See Also</span></span>

- [<span data-ttu-id="bedac-112">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="bedac-112">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="bedac-113">EncodeIntoBitFlipCode를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bedac-113">Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode</span></span>](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)