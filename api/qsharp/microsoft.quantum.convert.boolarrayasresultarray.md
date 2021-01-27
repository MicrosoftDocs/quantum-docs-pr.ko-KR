---
uid: Microsoft.Quantum.Convert.BoolArrayAsResultArray
title: BoolArrayAsResultArray 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsResultArray
qsharp.summary: Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.
ms.openlocfilehash: b30da07272ee1a6c19ae13afa618ba5deb7aaa2d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834185"
---
# <a name="boolarrayasresultarray-function"></a><span data-ttu-id="7b831-102">BoolArrayAsResultArray 함수</span><span class="sxs-lookup"><span data-stu-id="7b831-102">BoolArrayAsResultArray function</span></span>

<span data-ttu-id="7b831-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="7b831-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="7b831-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7b831-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7b831-105">`Bool[]`형식을 형식으로 변환 `Result[]` `true` 합니다. 여기서은로 매핑되고는 `One` `false` 에 매핑됩니다 `Zero` .</span><span class="sxs-lookup"><span data-stu-id="7b831-105">Converts a `Bool[]` type to a `Result[]` type, where `true` is mapped to `One` and `false` is mapped to `Zero`.</span></span>

```qsharp
function BoolArrayAsResultArray (input : Bool[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="7b831-106">입력</span><span class="sxs-lookup"><span data-stu-id="7b831-106">Input</span></span>

### <a name="input--bool"></a><span data-ttu-id="7b831-107">input: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="7b831-107">input : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="7b831-108">`Bool[]` 변환 될입니다.</span><span class="sxs-lookup"><span data-stu-id="7b831-108">`Bool[]` to be converted.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="7b831-109">출력: __잘못 <Result> 된__[]</span><span class="sxs-lookup"><span data-stu-id="7b831-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="7b831-110">`input`를 나타내는 `Result[]`입니다.</span><span class="sxs-lookup"><span data-stu-id="7b831-110">A `Result[]` representing the `input`.</span></span>