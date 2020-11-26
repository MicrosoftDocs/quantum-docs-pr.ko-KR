---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipCode
title: BitFlipCode 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipCode
qsharp.summary: Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 2d0b50bd2467fc01caacbbcb22f98c59a2d13922
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201226"
---
# <a name="bitflipcode-function"></a><span data-ttu-id="d2738-102">BitFlipCode 함수</span><span class="sxs-lookup"><span data-stu-id="d2738-102">BitFlipCode function</span></span>

<span data-ttu-id="d2738-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d2738-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d2738-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d2738-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d2738-105">내부 증후군 측정을 사용 하 여 ⟦ 3, 1, 1 ⟧ 비트 대칭 코드 인코더 및 디코더를 나타내는 QECC 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2738-105">Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function BitFlipCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="d2738-106">출력: [Qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="d2738-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="d2738-107">형식을 지정 하 여 퀀텀 오류 수정 코드의 구현을 반환 합니다 `QECC` .</span><span class="sxs-lookup"><span data-stu-id="d2738-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>