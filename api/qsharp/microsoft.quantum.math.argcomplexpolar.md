---
uid: Microsoft.Quantum.Math.ArgComplexPolar
title: ArgComplexPolar 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplexPolar
qsharp.summary: Returns the phase of a complex number of type `ComplexPolar`.
ms.openlocfilehash: 7088397bd60e2779ef60afc1bb7108d937a62c97
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195769"
---
# <a name="argcomplexpolar-function"></a><span data-ttu-id="45592-102">ArgComplexPolar 함수</span><span class="sxs-lookup"><span data-stu-id="45592-102">ArgComplexPolar function</span></span>

<span data-ttu-id="45592-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="45592-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="45592-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="45592-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="45592-105">복소수 형식의 단계를 반환 합니다 `ComplexPolar` .</span><span class="sxs-lookup"><span data-stu-id="45592-105">Returns the phase of a complex number of type `ComplexPolar`.</span></span>

```qsharp
function ArgComplexPolar (input : Microsoft.Quantum.Math.ComplexPolar) : Double
```


## <a name="input"></a><span data-ttu-id="45592-106">입력</span><span class="sxs-lookup"><span data-stu-id="45592-106">Input</span></span>

### <a name="input--complexpolar"></a><span data-ttu-id="45592-107">입력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="45592-107">input : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="45592-108">복소수 $c = r e ^ {i t} $입니다.</span><span class="sxs-lookup"><span data-stu-id="45592-108">Complex number $c = r e^{i t}$.</span></span>



## <a name="output--double"></a><span data-ttu-id="45592-109">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="45592-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="45592-110">$ \Text{Arg} [c] = t $ 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="45592-110">Phase $\text{Arg}[c] = t$.</span></span>