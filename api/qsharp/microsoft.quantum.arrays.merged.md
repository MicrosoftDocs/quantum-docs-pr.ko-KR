---
uid: Microsoft.Quantum.Arrays.Merged
title: 병합 된 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: b3383f8a04e6fa23562aa81e5b911d06752f4fb5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220640"
---
# <a name="merged-function"></a><span data-ttu-id="b211c-102">병합 된 함수</span><span class="sxs-lookup"><span data-stu-id="b211c-102">Merged function</span></span>

<span data-ttu-id="b211c-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b211c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b211c-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b211c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b211c-105">정렬 된 두 배열이 지정 된 경우 정렬 된 순서에서 두 요소가 모두 포함 된 단일 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b211c-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="b211c-106">Merge sort에 의해 내부적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b211c-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="b211c-107">입력</span><span class="sxs-lookup"><span data-stu-id="b211c-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="b211c-108">비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b211c-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="b211c-109">left: ' t []</span><span class="sxs-lookup"><span data-stu-id="b211c-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="b211c-110">right: ' t []</span><span class="sxs-lookup"><span data-stu-id="b211c-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="b211c-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="b211c-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b211c-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b211c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b211c-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="b211c-113">'T</span></span>

