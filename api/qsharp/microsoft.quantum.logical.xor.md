---
uid: Microsoft.Quantum.Logical.Xor
title: Xor 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Xor
qsharp.summary: Returns the Boolean exclusive disjunction of two values.
ms.openlocfilehash: afb94bd1fd0b791a9a7d84bc28b0cc2baf9a0938
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197095"
---
# <a name="xor-function"></a><span data-ttu-id="c1e7b-102">Xor 함수</span><span class="sxs-lookup"><span data-stu-id="c1e7b-102">Xor function</span></span>

<span data-ttu-id="c1e7b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="c1e7b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="c1e7b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c1e7b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c1e7b-105">두 값의 부울 배타적 논리합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-105">Returns the Boolean exclusive disjunction of two values.</span></span>

```qsharp
function Xor (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="c1e7b-106">입력</span><span class="sxs-lookup"><span data-stu-id="c1e7b-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="c1e7b-107">a: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c1e7b-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c1e7b-108">고려해 야 할 첫 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="c1e7b-109">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c1e7b-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c1e7b-110">고려할 두 번째 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c1e7b-111">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c1e7b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c1e7b-112">`true` 및 중 하나만 이면이 고, 그렇지 않으면 `a` `b` `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-112">`true` if and only if exactly one of `a` and `b` is `true`.</span></span>