---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: FastHadamardTransformed 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855464"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="5c645-102">FastHadamardTransformed 함수</span><span class="sxs-lookup"><span data-stu-id="5c645-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="5c645-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="5c645-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="5c645-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5c645-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5c645-105">{-1,1}Yates의 메서드를 사용 하 여 인코딩의 부울 함수 변환의 변환을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c645-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="5c645-106">입력</span><span class="sxs-lookup"><span data-stu-id="5c645-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="5c645-107">func: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5c645-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5c645-108">{-1,1}인코딩의 테이블</span><span class="sxs-lookup"><span data-stu-id="5c645-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="5c645-109">Output: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5c645-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5c645-110">함수의 Spectral 계수</span><span class="sxs-lookup"><span data-stu-id="5c645-110">Spectral coefficients of the function</span></span>

## <a name="example"></a><span data-ttu-id="5c645-111">예제</span><span class="sxs-lookup"><span data-stu-id="5c645-111">Example</span></span>

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```