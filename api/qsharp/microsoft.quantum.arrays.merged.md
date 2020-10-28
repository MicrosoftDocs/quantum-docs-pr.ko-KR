---
uid: Microsoft.Quantum.Arrays.Merged
title: 병합 된 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: da15a36f8f057cdc15062c96070ec21becc4794a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719012"
---
# <a name="merged-function"></a><span data-ttu-id="0033b-102">병합 된 함수</span><span class="sxs-lookup"><span data-stu-id="0033b-102">Merged function</span></span>

<span data-ttu-id="0033b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0033b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0033b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0033b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0033b-105">정렬 된 두 배열이 지정 된 경우 정렬 된 순서에서 두 요소가 모두 포함 된 단일 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0033b-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="0033b-106">Merge sort에 의해 내부적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0033b-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="0033b-107">입력</span><span class="sxs-lookup"><span data-stu-id="0033b-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="0033b-108">비교: (' ' ')-> [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0033b-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="0033b-109">left: ' t []</span><span class="sxs-lookup"><span data-stu-id="0033b-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="0033b-110">right: ' t []</span><span class="sxs-lookup"><span data-stu-id="0033b-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="0033b-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="0033b-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0033b-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0033b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0033b-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="0033b-113">'T</span></span>

