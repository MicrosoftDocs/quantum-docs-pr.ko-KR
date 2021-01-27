---
uid: Microsoft.Quantum.Logical.LessThanLexographic
title: LessThanLexographic 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanLexographic
qsharp.summary: Used to implement `LexographicComparison`.
ms.openlocfilehash: 716f58b747e9f58c338670271bb2e7aed96fe98c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815638"
---
# <a name="lessthanlexographic-function"></a><span data-ttu-id="44f9f-102">LessThanLexographic 함수</span><span class="sxs-lookup"><span data-stu-id="44f9f-102">LessThanLexographic function</span></span>

<span data-ttu-id="44f9f-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="44f9f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="44f9f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="44f9f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="44f9f-105">을 구현 하는 데 사용 `LexographicComparison` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44f9f-105">Used to implement `LexographicComparison`.</span></span>

```qsharp
function LessThanLexographic<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="44f9f-106">입력</span><span class="sxs-lookup"><span data-stu-id="44f9f-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="44f9f-107">비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="44f9f-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="44f9f-108">left: ' t []</span><span class="sxs-lookup"><span data-stu-id="44f9f-108">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="44f9f-109">right: ' t []</span><span class="sxs-lookup"><span data-stu-id="44f9f-109">right : 'T[]</span></span>





## <a name="output--bool"></a><span data-ttu-id="44f9f-110">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="44f9f-110">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="44f9f-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="44f9f-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="44f9f-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="44f9f-112">'T</span></span>

