---
uid: Microsoft.Quantum.Logical.EqualCP
title: EqualCP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualCP
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 83bf5ba245038ad1c7c6ed4e8cdb493317276e6a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817151"
---
# <a name="equalcp-function"></a><span data-ttu-id="4cd8d-102">EqualCP 함수</span><span class="sxs-lookup"><span data-stu-id="4cd8d-102">EqualCP function</span></span>

<span data-ttu-id="4cd8d-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="4cd8d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="4cd8d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4cd8d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4cd8d-105">두 입력이 같으면 true를 반환 하 고,</span><span class="sxs-lookup"><span data-stu-id="4cd8d-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="4cd8d-106">입력</span><span class="sxs-lookup"><span data-stu-id="4cd8d-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="4cd8d-107">a: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="4cd8d-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="4cd8d-108">비교할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd8d-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="4cd8d-109">b: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="4cd8d-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="4cd8d-110">비교할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd8d-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4cd8d-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4cd8d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4cd8d-112">`true` 가와 같으면이 고, 그렇지 않으면입니다 `a` `b` .</span><span class="sxs-lookup"><span data-stu-id="4cd8d-112">`true` if and only if `a` is equal to `b`.</span></span>