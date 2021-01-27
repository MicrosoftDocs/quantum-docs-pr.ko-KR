---
uid: Microsoft.Quantum.Core.RangeStart
title: 범위 시작 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 5b04e8c860a4bd6af7b10b4dbf803b1eb69ef5d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831111"
---
# <a name="rangestart-function"></a><span data-ttu-id="c975a-102">범위 시작 함수</span><span class="sxs-lookup"><span data-stu-id="c975a-102">RangeStart function</span></span>

<span data-ttu-id="c975a-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="c975a-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="c975a-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c975a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c975a-105">지정 된 범위의 정의 된 시작 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c975a-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="c975a-106">입력</span><span class="sxs-lookup"><span data-stu-id="c975a-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="c975a-107">범위: [범위](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="c975a-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="c975a-108">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c975a-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c975a-109">지정 된 범위의 정의 된 시작 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c975a-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="c975a-110">설명</span><span class="sxs-lookup"><span data-stu-id="c975a-110">Remarks</span></span>

<span data-ttu-id="c975a-111">범위 식의 첫 번째 요소는이 `start` `start+step` `start+step+step` 전달 될 때까지, 두 번째 요소는, 세 번째 요소는 등입니다. `end`</span><span class="sxs-lookup"><span data-stu-id="c975a-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="c975a-112">범위에서 정의 된 시작 값은 범위에서 빈 시퀀스 (예: 2.)를 지정 하는 경우를 제외 하 고는 시퀀스의 첫 번째 요소와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="c975a-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="c975a-113">1).</span><span class="sxs-lookup"><span data-stu-id="c975a-113">1).</span></span>