---
uid: Microsoft.Quantum.Synthesis.Extended
title: 확장 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: f8310a229205d8e870e3ca9253928d8a4a0520e7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230993"
---
# <a name="extended-function"></a><span data-ttu-id="24d14-102">확장 함수</span><span class="sxs-lookup"><span data-stu-id="24d14-102">Extended function</span></span>

<span data-ttu-id="24d14-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="24d14-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="24d14-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="24d14-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="24d14-105">반전 계수를 기준으로 스펙트럼 확장</span><span class="sxs-lookup"><span data-stu-id="24d14-105">Extends a spectrum by inverted coefficients</span></span>

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="24d14-106">입력</span><span class="sxs-lookup"><span data-stu-id="24d14-106">Input</span></span>

### <a name="spectrum--int"></a><span data-ttu-id="24d14-107">스펙트럼: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="24d14-107">spectrum : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="24d14-108">Spectral 계수</span><span class="sxs-lookup"><span data-stu-id="24d14-108">Spectral coefficients</span></span>



## <a name="output--int"></a><span data-ttu-id="24d14-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="24d14-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="24d14-110">계수와 반전 된 복사</span><span class="sxs-lookup"><span data-stu-id="24d14-110">Coefficients followed by inverted copy</span></span>