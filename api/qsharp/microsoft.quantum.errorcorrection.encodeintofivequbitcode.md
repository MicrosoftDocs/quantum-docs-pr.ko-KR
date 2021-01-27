---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: EncodeIntoFiveQubitCode 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 1bccf46453ad34199dcebc5bcff693359fe2254c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826314"
---
# <a name="encodeintofivequbitcode-operation"></a><span data-ttu-id="34130-102">EncodeIntoFiveQubitCode 작업</span><span class="sxs-lookup"><span data-stu-id="34130-102">EncodeIntoFiveQubitCode operation</span></span>

<span data-ttu-id="34130-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="34130-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="34130-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="34130-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="34130-105">⟦ 5, 1, 3 ⟧ 퀀텀 코드로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="34130-105">Encodes into the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="34130-106">입력</span><span class="sxs-lookup"><span data-stu-id="34130-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="34130-107">physRegister: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="34130-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="34130-108">인코딩되지 않은 상태를 나타내는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="34130-108">A qubit representing an unencoded state.</span></span> <span data-ttu-id="34130-109">이 배열의 `Qubit[]` 길이는 1입니다.</span><span class="sxs-lookup"><span data-stu-id="34130-109">This array `Qubit[]` is of length 1.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="34130-110">auxQubits: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="34130-110">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="34130-111">인코딩된 상태를 나타내는 데 사용 되는 보조 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="34130-111">A register of auxiliary qubits that will be used to represent the encoded state.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="34130-112">출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="34130-112">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="34130-113">`LogicalRegister`인코딩된 상태를 저장 하는 형식의 실제 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="34130-113">An array of physical qubits of type `LogicalRegister` that store the encoded state.</span></span>

## <a name="see-also"></a><span data-ttu-id="34130-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="34130-114">See Also</span></span>

- [<span data-ttu-id="34130-115">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="34130-115">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)