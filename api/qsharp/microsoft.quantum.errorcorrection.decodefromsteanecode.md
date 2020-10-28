---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: DecodeFromSteaneCode 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e6831a8630c0a80c2abe7c4a720263f0de03edc4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712419"
---
# <a name="decodefromsteanecode-operation"></a><span data-ttu-id="3e59e-102">DecodeFromSteaneCode 작업</span><span class="sxs-lookup"><span data-stu-id="3e59e-102">DecodeFromSteaneCode operation</span></span>

<span data-ttu-id="3e59e-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="3e59e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="3e59e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3e59e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3e59e-105">⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드 아래의 인코딩된 퀀텀 레지스터에 인코딩되지 않은 퀀텀 레지스터를 매핑하는 역 인코딩 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3e59e-105">An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="3e59e-106">입력</span><span class="sxs-lookup"><span data-stu-id="3e59e-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="3e59e-107">logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="3e59e-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="3e59e-108">인코딩된 5-고 비트 코드 논리 상태를 나타내는 정수 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="3e59e-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="3e59e-109">Output[: ((),](xref:microsoft.quantum.lang-ref.qubit)[[], [](xref:microsoft.quantum.lang-ref.qubit)])</span><span class="sxs-lookup"><span data-stu-id="3e59e-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="3e59e-110">첫 번째 매개 변수에서 인코딩되지 않은 상태를 나타내고 두 번째 매개 변수에서 보조 비트를 사용 하 여 길이가 1 인의 비트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="3e59e-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e59e-111">설명</span><span class="sxs-lookup"><span data-stu-id="3e59e-111">Remarks</span></span>

<span data-ttu-id="3e59e-112">선택한 디코더는 ⟦ 7, 1, 3 ⟧ Steane 코드의 CSS 코드 속성을 사용 합니다. 즉, X 오류 및 Z 오류를 별도로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e59e-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="3e59e-113">코드의 속성은 각각 정수로 간주 되는 경우 z 증후군 각각 x의 3 비트 인코딩입니다 (각각 z)을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e59e-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="3e59e-114">참조</span><span class="sxs-lookup"><span data-stu-id="3e59e-114">References</span></span>

- <span data-ttu-id="3e59e-115">D.</span><span class="sxs-lookup"><span data-stu-id="3e59e-115">D.</span></span> <span data-ttu-id="3e59e-116">Gottesman, "안정기 코드 및 퀀텀 오류 수정", "Ph.D Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="3e59e-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="3e59e-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3e59e-117">See Also</span></span>

- [<span data-ttu-id="3e59e-118">SteaneCodeEncoder를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e59e-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [<span data-ttu-id="3e59e-119">SteaneCodeDecoder를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e59e-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [<span data-ttu-id="3e59e-120">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="3e59e-120">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)