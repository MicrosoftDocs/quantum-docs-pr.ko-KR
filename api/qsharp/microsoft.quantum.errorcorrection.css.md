---
uid: Microsoft.Quantum.ErrorCorrection.CSS
title: CSS 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: CSS
qsharp.summary: Represents a Calderbank–Shor–Steane (CSS) code as defined by its encoder, decoder, and its syndrome measurement procedures for `X` and `Z` errors, respectively.
ms.openlocfilehash: c5227c771ec2c7c81d05a28681745af641eebeaf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712489"
---
# <a name="css-user-defined-type"></a><span data-ttu-id="528ad-102">CSS 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="528ad-102">CSS user defined type</span></span>

<span data-ttu-id="528ad-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="528ad-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="528ad-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="528ad-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="528ad-105">각각 및 오류에 대 한 인코더, 디코더 및 해당 증후군 측정 절차에서 정의한 대로 Calderbank – Shor – Steane (CSS) 코드를 나타냅니다 `X` `Z` .</span><span class="sxs-lookup"><span data-stu-id="528ad-105">Represents a Calderbank–Shor–Steane (CSS) code as defined by its encoder, decoder, and its syndrome measurement procedures for `X` and `Z` errors, respectively.</span></span>

```qsharp

newtype CSS = (Microsoft.Quantum.ErrorCorrection.EncodeOp, Microsoft.Quantum.ErrorCorrection.DecodeOp, Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp, Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp);
```

