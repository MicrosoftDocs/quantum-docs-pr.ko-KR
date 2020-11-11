---
uid: Microsoft.Quantum.Measurement.MResetZ
title: MResetZ 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 9f084b03504deea9fcf25e4c797c4bde3c97a995
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711054"
---
# <a name="mresetz-operation"></a><span data-ttu-id="0d136-102">MResetZ 작업</span><span class="sxs-lookup"><span data-stu-id="0d136-102">MResetZ operation</span></span>

<span data-ttu-id="0d136-103">네임 스페이스: [Microsoft 양자 측정](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="0d136-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="0d136-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d136-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d136-105">Z 단위로 단일 비트를 측정 하 고, 측정값을 따라 고정 된 초기 상태로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d136-105">Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.</span></span>

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a><span data-ttu-id="0d136-106">Description</span><span class="sxs-lookup"><span data-stu-id="0d136-106">Description</span></span>

<span data-ttu-id="0d136-107">$Z $ 기준으로 단일 비트 측정을 수행 하 고, 측정값을 따라 $ \ket $로이를 반환 하는지 확인 {0} 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d136-107">Performs a single-qubit measurement in the $Z$-basis, and ensures that the qubit is returned to $\ket{0}$ following the measurement.</span></span>

## <a name="input"></a><span data-ttu-id="0d136-108">입력</span><span class="sxs-lookup"><span data-stu-id="0d136-108">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="0d136-109">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0d136-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0d136-110">측정할 단일 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="0d136-110">A single qubit to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="0d136-111">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="0d136-111">Output : __invalid<Result>__</span></span>

<span data-ttu-id="0d136-112">`target`Pauli $Z $ 기준으로 측정 한 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="0d136-112">The result of measuring `target` in the Pauli $Z$ basis.</span></span>