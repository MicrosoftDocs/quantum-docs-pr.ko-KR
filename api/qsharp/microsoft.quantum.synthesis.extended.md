---
uid: Microsoft.Quantum.Synthesis.Extended
title: 확장 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855466"
---
# <a name="extended-function"></a><span data-ttu-id="1dc95-102">확장 함수</span><span class="sxs-lookup"><span data-stu-id="1dc95-102">Extended function</span></span>

<span data-ttu-id="1dc95-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="1dc95-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="1dc95-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1dc95-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1dc95-105">반전 계수를 기준으로 스펙트럼 확장</span><span class="sxs-lookup"><span data-stu-id="1dc95-105">Extends a spectrum by inverted coefficients</span></span>

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="1dc95-106">입력</span><span class="sxs-lookup"><span data-stu-id="1dc95-106">Input</span></span>

### <a name="spectrum--int"></a><span data-ttu-id="1dc95-107">스펙트럼: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1dc95-107">spectrum : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1dc95-108">Spectral 계수</span><span class="sxs-lookup"><span data-stu-id="1dc95-108">Spectral coefficients</span></span>



## <a name="output--int"></a><span data-ttu-id="1dc95-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1dc95-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1dc95-110">계수와 반전 된 복사</span><span class="sxs-lookup"><span data-stu-id="1dc95-110">Coefficients followed by inverted copy</span></span>

## <a name="example"></a><span data-ttu-id="1dc95-111">예제</span><span class="sxs-lookup"><span data-stu-id="1dc95-111">Example</span></span>

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```