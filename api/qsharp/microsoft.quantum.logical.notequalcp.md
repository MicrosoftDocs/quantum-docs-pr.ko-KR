---
uid: Microsoft.Quantum.Logical.NotEqualCP
title: NotEqualCP 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualCP
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: df735408f76eb6b88f0d867021d69b83edd69b7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197299"
---
# <a name="notequalcp-function"></a><span data-ttu-id="dc821-102">NotEqualCP 함수</span><span class="sxs-lookup"><span data-stu-id="dc821-102">NotEqualCP function</span></span>

<span data-ttu-id="dc821-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="dc821-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="dc821-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dc821-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dc821-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc821-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="dc821-106">입력</span><span class="sxs-lookup"><span data-stu-id="dc821-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="dc821-107">a: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="dc821-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="dc821-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dc821-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="dc821-109">b: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="dc821-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="dc821-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dc821-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="dc821-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dc821-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dc821-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="dc821-112">`true` if and only if `a` is not equal to `b`.</span></span>