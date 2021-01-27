---
uid: Microsoft.Quantum.Math.ModulusI
title: ModulusI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 7bad044db9e2229c85cb3909dc4802bceaee6382
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847300"
---
# <a name="modulusi-function"></a><span data-ttu-id="b7e17-102">ModulusI 함수</span><span class="sxs-lookup"><span data-stu-id="b7e17-102">ModulusI function</span></span>

<span data-ttu-id="b7e17-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b7e17-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b7e17-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b7e17-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b7e17-105">모듈로 정식 residue을 계산 `value` `modulus` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e17-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="b7e17-106">입력</span><span class="sxs-lookup"><span data-stu-id="b7e17-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="b7e17-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b7e17-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b7e17-108">Residue 계산 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e17-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="b7e17-109">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b7e17-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b7e17-110">Residues를 사용 하는 모듈러스는 양수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e17-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="b7e17-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b7e17-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b7e17-112">`modulus - 1` `value - r` 모듈러스로 나눌 수 있는 0에서 사이의 정수 $r $</span><span class="sxs-lookup"><span data-stu-id="b7e17-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e17-113">설명</span><span class="sxs-lookup"><span data-stu-id="b7e17-113">Remarks</span></span>

<span data-ttu-id="b7e17-114">이 함수는 c #에서 연산자가 작동 하는 방식과 다른 방식으로 동작 `%` 하며 `modulus - 1` , 값이 음수인 경우에도 결과에는 항상 0과 사이의 음수가 아닌 정수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e17-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a non-negative integer between 0 and `modulus - 1`, even if value is negative.</span></span>