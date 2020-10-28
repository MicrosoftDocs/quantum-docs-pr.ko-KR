---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: DecodeFromFiveQubitCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 421da6296b604f30aefed58730091f64f19c3a61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712468"
---
# <a name="decodefromfivequbitcode-operation"></a><span data-ttu-id="fda24-102">DecodeFromFiveQubitCode 작업</span><span class="sxs-lookup"><span data-stu-id="fda24-102">DecodeFromFiveQubitCode operation</span></span>

<span data-ttu-id="fda24-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="fda24-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="fda24-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fda24-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fda24-105">⟦ 5, 1, 3 ⟧ 퀀텀 코드를 디코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="fda24-105">Decodes the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="fda24-106">입력</span><span class="sxs-lookup"><span data-stu-id="fda24-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="fda24-107">logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="fda24-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="fda24-108">인코딩된 5-고 비트 코드 논리 상태를 나타내는 정수 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fda24-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="fda24-109">Output[: ((),](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)])</span><span class="sxs-lookup"><span data-stu-id="fda24-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="fda24-110">첫 번째 매개 변수에서 인코딩되지 않은 상태를 나타내고 두 번째 매개 변수에서 보조 비트를 사용 하 여 길이가 1 인의 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fda24-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="fda24-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fda24-111">See Also</span></span>

- [<span data-ttu-id="fda24-112">Microsoft 양자 수정. FiveQubitCodeEncoder</span><span class="sxs-lookup"><span data-stu-id="fda24-112">Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [<span data-ttu-id="fda24-113">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="fda24-113">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)