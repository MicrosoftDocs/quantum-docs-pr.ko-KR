---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: SteaneCodeRecoveryX 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 0f6b987ca23bd9ff2076080d60f1ca756b36848e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712132"
---
# <a name="steanecoderecoveryx-function"></a><span data-ttu-id="2ac8e-102">SteaneCodeRecoveryX 함수</span><span class="sxs-lookup"><span data-stu-id="2ac8e-102">SteaneCodeRecoveryX function</span></span>

<span data-ttu-id="2ac8e-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="2ac8e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="2ac8e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2ac8e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2ac8e-105">⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드의 안정기 그룹에 있는 X 부분에 대 한 디코더입니다.</span><span class="sxs-lookup"><span data-stu-id="2ac8e-105">Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="2ac8e-106">입력</span><span class="sxs-lookup"><span data-stu-id="2ac8e-106">Input</span></span>

### <a name="syndrome--syndrome"></a><span data-ttu-id="2ac8e-107">증후군: [증후군](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="2ac8e-107">syndrome : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="2ac8e-108">안정기의 X 부분을 측정 하 여 가져온 증후군 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2ac8e-108">A syndrome array obtained from measuring the X-part of the stabilizer.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="2ac8e-109">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="2ac8e-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="2ac8e-110">인코딩된 퀀텀 시스템에 적용 될 때에 해당 하는 오류를 수정 하는 Pauli 작업의 배열입니다 `syndrome` .</span><span class="sxs-lookup"><span data-stu-id="2ac8e-110">An array of Pauli operations which, when applied to the encoded quantum system corrects the error corresponding to `syndrome`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ac8e-111">설명</span><span class="sxs-lookup"><span data-stu-id="2ac8e-111">Remarks</span></span>

<span data-ttu-id="2ac8e-112">선택한 디코더는 ⟦ 7, 1, 3 ⟧ Steane 코드의 CSS 코드 속성을 사용 합니다. 즉, X 오류 및 Z 오류를 별도로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac8e-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="2ac8e-113">코드의 속성은 각각 정수로 간주 되는 경우 z 증후군 각각 x의 3 비트 인코딩입니다 (각각 z)을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac8e-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="2ac8e-114">참조</span><span class="sxs-lookup"><span data-stu-id="2ac8e-114">References</span></span>

- <span data-ttu-id="2ac8e-115">D.</span><span class="sxs-lookup"><span data-stu-id="2ac8e-115">D.</span></span> <span data-ttu-id="2ac8e-116">Gottesman, "안정기 코드 및 퀀텀 오류 수정", "Ph.D Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="2ac8e-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="2ac8e-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2ac8e-117">See Also</span></span>

- [<span data-ttu-id="2ac8e-118">SteaneCodeRecoveryX를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac8e-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="2ac8e-119">SteaneCodeRecoveryFns를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ac8e-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)