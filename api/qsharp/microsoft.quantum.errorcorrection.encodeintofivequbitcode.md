---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: EncodeIntoFiveQubitCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: c9df4c5c98a78cae8b3af4597020d35469454153
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712398"
---
# <a name="encodeintofivequbitcode-operation"></a><span data-ttu-id="ff306-102">EncodeIntoFiveQubitCode 작업</span><span class="sxs-lookup"><span data-stu-id="ff306-102">EncodeIntoFiveQubitCode operation</span></span>

<span data-ttu-id="ff306-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="ff306-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="ff306-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ff306-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ff306-105">⟦ 5, 1, 3 ⟧ 퀀텀 코드로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="ff306-105">Encodes into the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="ff306-106">입력</span><span class="sxs-lookup"><span data-stu-id="ff306-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="ff306-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ff306-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ff306-108">인코딩되지 않은 상태를 나타내는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="ff306-108">A qubit representing an unencoded state.</span></span> <span data-ttu-id="ff306-109">이 배열의 `Qubit[]` 길이는 1입니다.</span><span class="sxs-lookup"><span data-stu-id="ff306-109">This array `Qubit[]` is of length 1.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="ff306-110">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ff306-110">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ff306-111">인코딩된 상태를 나타내는 데 사용 되는 보조 비트의 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="ff306-111">A register of auxiliary qubits that will be used to represent the encoded state.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="ff306-112">출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="ff306-112">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="ff306-113">`LogicalRegister`인코딩된 상태를 저장 하는 형식의 실제 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ff306-113">An array of physical qubits of type `LogicalRegister` that store the encoded state.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff306-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ff306-114">See Also</span></span>

- [<span data-ttu-id="ff306-115">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="ff306-115">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)