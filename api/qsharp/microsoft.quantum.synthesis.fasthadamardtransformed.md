---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: FastHadamardTransformed 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 2b84e92d08a3baad2552780cae91f447830cac82
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725184"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="96549-102">FastHadamardTransformed 함수</span><span class="sxs-lookup"><span data-stu-id="96549-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="96549-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="96549-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="96549-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="96549-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="96549-105">{-1,1}Yates의 메서드를 사용 하 여 인코딩의 부울 함수 변환의 변환을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="96549-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="96549-106">입력</span><span class="sxs-lookup"><span data-stu-id="96549-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="96549-107">func: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="96549-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="96549-108">{-1,1}인코딩의 테이블</span><span class="sxs-lookup"><span data-stu-id="96549-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="96549-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="96549-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="96549-110">함수의 Spectral 계수</span><span class="sxs-lookup"><span data-stu-id="96549-110">Spectral coefficients of the function</span></span>