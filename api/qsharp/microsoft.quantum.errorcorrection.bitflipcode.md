---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipCode
title: BitFlipCode 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipCode
qsharp.summary: Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 8d4498647682026e9dec3fa96cfb69ba1e3214b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712503"
---
# <a name="bitflipcode-function"></a><span data-ttu-id="8fd5b-102">BitFlipCode 함수</span><span class="sxs-lookup"><span data-stu-id="8fd5b-102">BitFlipCode function</span></span>

<span data-ttu-id="8fd5b-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="8fd5b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="8fd5b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8fd5b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8fd5b-105">내부 증후군 측정을 사용 하 여 ⟦ 3, 1, 1 ⟧ 비트 대칭 코드 인코더 및 디코더를 나타내는 QECC 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd5b-105">Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function BitFlipCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="8fd5b-106">출력: [Qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="8fd5b-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="8fd5b-107">형식을 지정 하 여 퀀텀 오류 수정 코드의 구현을 반환 합니다 `QECC` .</span><span class="sxs-lookup"><span data-stu-id="8fd5b-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>