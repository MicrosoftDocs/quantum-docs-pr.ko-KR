---
uid: Microsoft.Quantum.Synthesis.SizeAdjustedTruthTable
title: SizeAdjustedTruthTable 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: SizeAdjustedTruthTable
qsharp.summary: >-
  Adjusts truth table from array of Booleans according to number of variables

  A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.
ms.openlocfilehash: 8d69aa119c25a0f64743fec36c00ecdef2450c44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855316"
---
# <a name="sizeadjustedtruthtable-function"></a><span data-ttu-id="190b5-102">SizeAdjustedTruthTable 함수</span><span class="sxs-lookup"><span data-stu-id="190b5-102">SizeAdjustedTruthTable function</span></span>

<span data-ttu-id="190b5-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="190b5-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="190b5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="190b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="190b5-105">변수의 수에 따라 부울의 배열에서 참 테이블을 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="190b5-105">Adjusts truth table from array of Booleans according to number of variables</span></span>

<span data-ttu-id="190b5-106">새 배열은 길이가 반환 되며 항목을 `2^numVars` `table` 사용 하 여 크기를 확장 `false` 하거나 요소로 자를 수 있습니다 `2^numVars` .</span><span class="sxs-lookup"><span data-stu-id="190b5-106">A new array is returned of length `2^numVars`, possibly requiring to extend `table`'s size with `false` entries or truncating it to `2^numVars` elements.</span></span>

```qsharp
function SizeAdjustedTruthTable (table : Bool[], numVars : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="190b5-107">입력</span><span class="sxs-lookup"><span data-stu-id="190b5-107">Input</span></span>

### <a name="table--bool"></a><span data-ttu-id="190b5-108">테이블: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="190b5-108">table : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="190b5-109">참 테이블을 실제 값 배열로</span><span class="sxs-lookup"><span data-stu-id="190b5-109">Truth table as array of truth values</span></span>


### <a name="numvars--int"></a><span data-ttu-id="190b5-110">numVars: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="190b5-110">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="190b5-111">변수 수</span><span class="sxs-lookup"><span data-stu-id="190b5-111">Number of variables</span></span>



## <a name="output--bool"></a><span data-ttu-id="190b5-112">Output: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="190b5-112">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="190b5-113">크기 조정 참 테이블</span><span class="sxs-lookup"><span data-stu-id="190b5-113">Size adjusted truth table</span></span>