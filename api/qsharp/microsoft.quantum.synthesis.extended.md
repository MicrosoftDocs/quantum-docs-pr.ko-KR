---
uid: Microsoft.Quantum.Synthesis.Extended
title: 확장 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 9109a05c795f351a4973e1600ce291cdeb94a280
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725191"
---
# <a name="extended-function"></a><span data-ttu-id="f4c31-102">확장 함수</span><span class="sxs-lookup"><span data-stu-id="f4c31-102">Extended function</span></span>

<span data-ttu-id="f4c31-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f4c31-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f4c31-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f4c31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f4c31-105">반전 계수를 기준으로 스펙트럼 확장</span><span class="sxs-lookup"><span data-stu-id="f4c31-105">Extends a spectrum by inverted coefficients</span></span>

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="f4c31-106">입력</span><span class="sxs-lookup"><span data-stu-id="f4c31-106">Input</span></span>

### <a name="spectrum--int"></a><span data-ttu-id="f4c31-107">스펙트럼: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f4c31-107">spectrum : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f4c31-108">Spectral 계수</span><span class="sxs-lookup"><span data-stu-id="f4c31-108">Spectral coefficients</span></span>



## <a name="output--int"></a><span data-ttu-id="f4c31-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f4c31-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f4c31-110">계수와 반전 된 복사</span><span class="sxs-lookup"><span data-stu-id="f4c31-110">Coefficients followed by inverted copy</span></span>