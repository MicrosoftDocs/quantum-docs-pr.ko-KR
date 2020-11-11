---
uid: Microsoft.Quantum.ErrorCorrection.QECC
title: QECC 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: QECC
qsharp.summary: Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.
ms.openlocfilehash: 6a00875f53928da4e0b8da6a3e32e37a551a56b2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712251"
---
# <a name="qecc-user-defined-type"></a><span data-ttu-id="8ed12-102">QECC 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="8ed12-102">QECC user defined type</span></span>

<span data-ttu-id="8ed12-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="8ed12-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="8ed12-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8ed12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8ed12-105">인코더, 디코더 및 증후군 측정 프로시저에 정의 된 오류 수정 코드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8ed12-105">Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.</span></span>

```qsharp

newtype QECC = (Microsoft.Quantum.ErrorCorrection.EncodeOp, Microsoft.Quantum.ErrorCorrection.DecodeOp, Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp);
```
