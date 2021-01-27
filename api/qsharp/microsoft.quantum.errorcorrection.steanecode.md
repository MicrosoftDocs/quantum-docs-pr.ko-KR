---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: SteaneCode 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: af3f3ef5088b898bd827ebca00fdc7fcb992f2a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853066"
---
# <a name="steanecode-function"></a><span data-ttu-id="61f73-102">SteaneCode 함수</span><span class="sxs-lookup"><span data-stu-id="61f73-102">SteaneCode function</span></span>

<span data-ttu-id="61f73-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="61f73-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="61f73-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="61f73-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="61f73-105">내부 증후군 측정을 포함 하는 ⟦ 7, 1, 3 ⟧ Steane 코드 인코더 및 디코더를 나타내는 CSS 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="61f73-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="61f73-106">출력: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="61f73-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="61f73-107">⟦ 7, 1, 3 ⟧ Steane 코드에 대 한 인코딩 및 오류 수정을 수행 하기 위해 모든 관련 데이터를 수집 하는 CSS 형식의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="61f73-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61f73-108">설명</span><span class="sxs-lookup"><span data-stu-id="61f73-108">Remarks</span></span>

<span data-ttu-id="61f73-109">이 코드는 다음 문서에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61f73-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="61f73-110">A.</span><span class="sxs-lookup"><span data-stu-id="61f73-110">A.</span></span> <span data-ttu-id="61f73-111">Steane, "다중 파티클 간섭 및 퀀텀 오류 수정", Proc.</span><span class="sxs-lookup"><span data-stu-id="61f73-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="61f73-112">Roy.</span><span class="sxs-lookup"><span data-stu-id="61f73-112">Roy.</span></span> <span data-ttu-id="61f73-113">Lond.</span><span class="sxs-lookup"><span data-stu-id="61f73-113">Soc. Lond.</span></span> <span data-ttu-id="61f73-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="61f73-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>