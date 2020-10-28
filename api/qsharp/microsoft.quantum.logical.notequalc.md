---
uid: Microsoft.Quantum.Logical.NotEqualC
title: NotEqualC 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualC
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: b26ad3515cb801b122858b9474aea76a0e5c498b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709822"
---
# <a name="notequalc-function"></a><span data-ttu-id="99261-102">NotEqualC 함수</span><span class="sxs-lookup"><span data-stu-id="99261-102">NotEqualC function</span></span>

<span data-ttu-id="99261-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="99261-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="99261-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="99261-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="99261-105">두 입력이 같지 않은 경우에만 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="99261-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualC (a : Microsoft.Quantum.Math.Complex, b : Microsoft.Quantum.Math.Complex) : Bool
```


## <a name="input"></a><span data-ttu-id="99261-106">입력</span><span class="sxs-lookup"><span data-stu-id="99261-106">Input</span></span>

### <a name="a--complex"></a><span data-ttu-id="99261-107">a: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="99261-107">a : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="99261-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="99261-108">The first value to be compared.</span></span>


### <a name="b--complex"></a><span data-ttu-id="99261-109">b: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="99261-109">b : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="99261-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="99261-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="99261-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="99261-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="99261-112">`true``a`가와 같지 않은 경우에만입니다 `b` .</span><span class="sxs-lookup"><span data-stu-id="99261-112">`true` if and only if `a` is not equal to `b`.</span></span>