---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: EncodeIntoSteaneCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 39b8ab549413d9d5281f6b84a6e970c45242fca8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712391"
---
# <a name="encodeintosteanecode-operation"></a><span data-ttu-id="268f3-102">EncodeIntoSteaneCode 작업</span><span class="sxs-lookup"><span data-stu-id="268f3-102">EncodeIntoSteaneCode operation</span></span>

<span data-ttu-id="268f3-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="268f3-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="268f3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="268f3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="268f3-105">⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드 아래의 인코딩된 퀀텀 레지스터에 인코딩되지 않은 퀀텀 레지스터를 매핑하는 인코딩 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="268f3-105">An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="268f3-106">입력</span><span class="sxs-lookup"><span data-stu-id="268f3-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="268f3-107">physRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="268f3-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="268f3-108">인코딩되지 않은 퀀텀 상태를 포함 하는 ubit 레지스터</span><span class="sxs-lookup"><span data-stu-id="268f3-108">A qubit register which holds the an unencoded quantum state</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="268f3-109">auxQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="268f3-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="268f3-110">처음에는 0이 고, 인코딩 작업을 수행할 수 있도록 퀀텀 시스템에 추가 되는 추가 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="268f3-110">A qubit register which is initially zero and which gets added to the quantum system so that an encoding operation can be performed</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="268f3-111">출력: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="268f3-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="268f3-112">Steane 인코더가 적용 된 후 상태를 포함 하는 퀀텀 레지스터</span><span class="sxs-lookup"><span data-stu-id="268f3-112">A quantum register holding the state after the Steane encoder has been applied</span></span>

## <a name="see-also"></a><span data-ttu-id="268f3-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="268f3-113">See Also</span></span>

- [<span data-ttu-id="268f3-114">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="268f3-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="268f3-115">SteaneCodeDecoder를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268f3-115">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)