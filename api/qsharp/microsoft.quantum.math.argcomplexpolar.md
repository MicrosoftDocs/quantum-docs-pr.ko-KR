---
uid: Microsoft.Quantum.Math.ArgComplexPolar
title: ArgComplexPolar 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplexPolar
qsharp.summary: Returns the phase of a complex number of type `ComplexPolar`.
ms.openlocfilehash: b4f2b9a192770f453302b469c80f03a9e57cf891
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723217"
---
# <a name="argcomplexpolar-function"></a><span data-ttu-id="669ab-102">ArgComplexPolar 함수</span><span class="sxs-lookup"><span data-stu-id="669ab-102">ArgComplexPolar function</span></span>

<span data-ttu-id="669ab-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="669ab-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="669ab-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="669ab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="669ab-105">복소수 형식의 단계를 반환 합니다 `ComplexPolar` .</span><span class="sxs-lookup"><span data-stu-id="669ab-105">Returns the phase of a complex number of type `ComplexPolar`.</span></span>

```qsharp
function ArgComplexPolar (input : Microsoft.Quantum.Math.ComplexPolar) : Double
```


## <a name="input"></a><span data-ttu-id="669ab-106">입력</span><span class="sxs-lookup"><span data-stu-id="669ab-106">Input</span></span>

### <a name="input--complexpolar"></a><span data-ttu-id="669ab-107">입력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="669ab-107">input : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="669ab-108">복소수 $c = r e ^ {i t} $입니다.</span><span class="sxs-lookup"><span data-stu-id="669ab-108">Complex number $c = r e^{i t}$.</span></span>



## <a name="output--double"></a><span data-ttu-id="669ab-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="669ab-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="669ab-110">$ \Text{Arg} [c] = t $ 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="669ab-110">Phase $\text{Arg}[c] = t$.</span></span>