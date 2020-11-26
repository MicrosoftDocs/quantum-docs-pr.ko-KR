---
uid: Microsoft.Quantum.Logical.LessThanLexographic
title: LessThanLexographic 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanLexographic
qsharp.summary: Used to implement `LexographicComparison`.
ms.openlocfilehash: 3b3ac3f9f8b70307099de60899c969abb2acad7c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197673"
---
# <a name="lessthanlexographic-function"></a><span data-ttu-id="440d9-102">LessThanLexographic 함수</span><span class="sxs-lookup"><span data-stu-id="440d9-102">LessThanLexographic function</span></span>

<span data-ttu-id="440d9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="440d9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="440d9-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="440d9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="440d9-105">을 구현 하는 데 사용 `LexographicComparison` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="440d9-105">Used to implement `LexographicComparison`.</span></span>

```qsharp
function LessThanLexographic<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="440d9-106">입력</span><span class="sxs-lookup"><span data-stu-id="440d9-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="440d9-107">비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="440d9-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="440d9-108">left: ' t []</span><span class="sxs-lookup"><span data-stu-id="440d9-108">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="440d9-109">right: ' t []</span><span class="sxs-lookup"><span data-stu-id="440d9-109">right : 'T[]</span></span>





## <a name="output--bool"></a><span data-ttu-id="440d9-110">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="440d9-110">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="440d9-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="440d9-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="440d9-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="440d9-112">'T</span></span>

