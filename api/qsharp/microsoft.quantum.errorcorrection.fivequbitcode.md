---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: FiveQubitCode 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 3b45af29897735905f7fe52340e2a8e425bd8cbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200886"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="ffbd9-102">FiveQubitCode 함수</span><span class="sxs-lookup"><span data-stu-id="ffbd9-102">FiveQubitCode function</span></span>

<span data-ttu-id="ffbd9-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="ffbd9-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="ffbd9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ffbd9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ffbd9-105">내부 증후군 측정을 포함 하는 ⟦ 5, 1, 3 ⟧ 코드 인코더 및 디코더를 나타내는 QECC 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="ffbd9-106">출력: [Qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="ffbd9-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="ffbd9-107">형식을 지정 하 여 퀀텀 오류 수정 코드의 구현을 반환 합니다 `QECC` .</span><span class="sxs-lookup"><span data-stu-id="ffbd9-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffbd9-108">설명</span><span class="sxs-lookup"><span data-stu-id="ffbd9-108">Remarks</span></span>

<span data-ttu-id="ffbd9-109">이 코드는 다음 두 가지 문서에 독립적으로 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="ffbd9-110">C.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-110">C.</span></span> <span data-ttu-id="ffbd9-111">H.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-111">H.</span></span> <span data-ttu-id="ffbd9-112">DiVincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="ffbd9-113">Smolin 및 W. K입니다.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-113">Smolin and W. K.</span></span> <span data-ttu-id="ffbd9-114">Wootters, "Mixed state 되거나 얽 히 및 퀀텀 오류 수정", "Phys, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 및</span><span class="sxs-lookup"><span data-stu-id="ffbd9-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="ffbd9-115">18.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-115">R.</span></span> <span data-ttu-id="ffbd9-116">Laflamme, c. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="ffbd9-117">합니다.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-117">Paz and W. H.</span></span> <span data-ttu-id="ffbd9-118">Zurek, "완전 한 퀀텀 오류 수정 코드", "Phys. Lett.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="ffbd9-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="ffbd9-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>