---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipCode
title: BitFlipCode 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipCode
qsharp.summary: Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 0a5a028f85b80575b754b93a797a1460d21bb552
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853201"
---
# <a name="bitflipcode-function"></a><span data-ttu-id="3221c-102">BitFlipCode 함수</span><span class="sxs-lookup"><span data-stu-id="3221c-102">BitFlipCode function</span></span>

<span data-ttu-id="3221c-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="3221c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="3221c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3221c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3221c-105">내부 증후군 측정을 사용 하 여 ⟦ 3, 1, 1 ⟧ 비트 대칭 코드 인코더 및 디코더를 나타내는 QECC 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3221c-105">Returns a QECC value representing the ⟦3, 1, 1⟧ bit flip code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function BitFlipCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="3221c-106">출력: [Qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="3221c-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="3221c-107">형식을 지정 하 여 퀀텀 오류 수정 코드의 구현을 반환 합니다 `QECC` .</span><span class="sxs-lookup"><span data-stu-id="3221c-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>