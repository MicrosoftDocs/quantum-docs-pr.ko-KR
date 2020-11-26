---
uid: Microsoft.Quantum.Math.ModulusI
title: ModulusI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6bbb3877b93e1fc6b38f85a716ba617311c7cfba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227780"
---
# <a name="modulusi-function"></a><span data-ttu-id="4075b-102">ModulusI 함수</span><span class="sxs-lookup"><span data-stu-id="4075b-102">ModulusI function</span></span>

<span data-ttu-id="4075b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4075b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4075b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4075b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4075b-105">모듈로 정식 residue을 계산 `value` `modulus` 합니다.</span><span class="sxs-lookup"><span data-stu-id="4075b-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="4075b-106">입력</span><span class="sxs-lookup"><span data-stu-id="4075b-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="4075b-107">값: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4075b-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4075b-108">Residue 계산 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4075b-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="4075b-109">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4075b-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4075b-110">Residues를 사용 하는 모듈러스는 양수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4075b-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="4075b-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4075b-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4075b-112">`modulus - 1` `value - r` 모듈러스로 나눌 수 있는 0에서 사이의 정수 $r $</span><span class="sxs-lookup"><span data-stu-id="4075b-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="4075b-113">설명</span><span class="sxs-lookup"><span data-stu-id="4075b-113">Remarks</span></span>

<span data-ttu-id="4075b-114">이 함수는 c #에서 연산자가 작동 하는 방식과 다른 방식으로 동작 `%` 하며 `modulus - 1` , 값이 음수인 경우에도 항상 0과 사이의 양의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="4075b-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>