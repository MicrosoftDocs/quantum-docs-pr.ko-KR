---
uid: Microsoft.Quantum.Measurement.MResetX
title: MResetX 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 04fb0f84ddf79a3d2cfc21fdaabd16c129f6d72f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194205"
---
# <a name="mresetx-operation"></a><span data-ttu-id="ddcbe-102">MResetX 작업</span><span class="sxs-lookup"><span data-stu-id="ddcbe-102">MResetX operation</span></span>

<span data-ttu-id="ddcbe-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="ddcbe-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="ddcbe-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ddcbe-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ddcbe-105">X 단위로 단일 계산 비트를 측정 하 고 측정값을 따라 고정 된 초기 상태로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-105">Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="ddcbe-106">Description</span><span class="sxs-lookup"><span data-stu-id="ddcbe-106">Description</span></span>

<span data-ttu-id="ddcbe-107">$X $ 기준으로 단일 비트 측정을 수행 하 고, 측정값을 따라 $ \ket $로이를 반환 하는지 확인 {0} 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-107">Performs a single-qubit measurement in the $X$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="ddcbe-108">입력</span><span class="sxs-lookup"><span data-stu-id="ddcbe-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="ddcbe-109">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ddcbe-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ddcbe-110">측정할 단일 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="ddcbe-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="ddcbe-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="ddcbe-112">`target`Pauli $X $ 기준으로 측정 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-112">The result of measuring `target` in the Pauli $X$ basis.</span></span>