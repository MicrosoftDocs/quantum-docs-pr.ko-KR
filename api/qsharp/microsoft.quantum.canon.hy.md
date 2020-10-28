---
uid: Microsoft.Quantum.Canon.HY
title: HY 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: HY
qsharp.summary: >-
  Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.

  The Y Hadamard transformation $H_Y = S H$ on a single qubit is:

  \begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}. \end{align}
ms.openlocfilehash: bc3417ff948b718be5b96513f30f3e2714b9e20c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716143"
---
# <a name="hy-operation"></a><span data-ttu-id="2e9e4-102">HY 작업</span><span class="sxs-lookup"><span data-stu-id="2e9e4-102">HY operation</span></span>

<span data-ttu-id="2e9e4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2e9e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2e9e4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e9e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e9e4-105">Z와 Y 축을 교환 하는 Hadamard 변환에 Y 기반 아날로그를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9e4-105">Applies the Y-basis analog to the Hadamard transformation that interchanges the Z and Y axes.</span></span>

<span data-ttu-id="2e9e4-106">단일의 비트에서 Y Hadamard 변환 $H _Y = S H $는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2e9e4-106">The Y Hadamard transformation $H_Y = S H$ on a single qubit is:</span></span>

<span data-ttu-id="2e9e4-107">\begin{align} H_Y \mathrel{: =} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ i &-i \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="2e9e4-107">\begin{align} H_Y \mathrel{:=} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ i & -i \end{bmatrix}.</span></span>
<span data-ttu-id="2e9e4-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2e9e4-108">\end{align}</span></span>

```qsharp
operation HY (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="2e9e4-109">입력</span><span class="sxs-lookup"><span data-stu-id="2e9e4-109">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="2e9e4-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2e9e4-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2e9e4-111">게이트가 적용 되어야 하는의 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9e4-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2e9e4-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e9e4-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="2e9e4-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2e9e4-113">See Also</span></span>

- [<span data-ttu-id="2e9e4-114">Microsoft 양자</span><span class="sxs-lookup"><span data-stu-id="2e9e4-114">Microsoft.Quantum.Intrinsic.H</span></span>](xref:Microsoft.Quantum.Intrinsic.H)