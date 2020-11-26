---
uid: Microsoft.Quantum.Measurement.MResetY
title: MResetY 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 36c6f227135b5ccaf1146fd7afdc8205d416c5dd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227032"
---
# <a name="mresety-operation"></a><span data-ttu-id="68941-102">MResetY 작업</span><span class="sxs-lookup"><span data-stu-id="68941-102">MResetY operation</span></span>

<span data-ttu-id="68941-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="68941-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="68941-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="68941-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="68941-105">Y를 기준으로 단일의 비트를 측정 하 고 측정 다음에 고정 된 초기 상태로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68941-105">Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="68941-106">설명</span><span class="sxs-lookup"><span data-stu-id="68941-106">Description</span></span>

<span data-ttu-id="68941-107">$Y $ 기준으로 단일 비트 측정을 수행 하 고, 측정값을 따라 $ \ket $로이를 반환 하는지 확인 {0} 합니다.</span><span class="sxs-lookup"><span data-stu-id="68941-107">Performs a single-qubit measurement in the $Y$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="68941-108">입력</span><span class="sxs-lookup"><span data-stu-id="68941-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="68941-109">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="68941-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="68941-110">측정할 단일 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="68941-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="68941-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="68941-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="68941-112">`target`Pauli $Y $ 기준으로 측정 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="68941-112">The result of measuring `target` in the Pauli $Y$ basis.</span></span>