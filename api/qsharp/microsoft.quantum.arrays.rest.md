---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: b6c579df354185a2defb08cd78bce816d8cc5959
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845471"
---
# <a name="rest-function"></a><span data-ttu-id="8fbce-102">Rest 함수</span><span class="sxs-lookup"><span data-stu-id="8fbce-102">Rest function</span></span>

<span data-ttu-id="8fbce-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8fbce-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8fbce-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fbce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fbce-105">첫 번째 배열 요소가 삭제 된 경우를 제외 하 고 입력 배열과 같은 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8fbce-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8fbce-106">입력</span><span class="sxs-lookup"><span data-stu-id="8fbce-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="8fbce-107">배열: ' t []</span><span class="sxs-lookup"><span data-stu-id="8fbce-107">array : 'T[]</span></span>

<span data-ttu-id="8fbce-108">마지막 요소에 대 한 두 번째 배열이 출력 배열을 구성 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbce-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="8fbce-109">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="8fbce-109">Output : 'T[]</span></span>

<span data-ttu-id="8fbce-110">요소를 포함 하는 배열 `array[1..Length(array) - 1]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbce-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8fbce-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8fbce-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8fbce-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="8fbce-112">'T</span></span>

<span data-ttu-id="8fbce-113">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbce-113">The type of the array elements.</span></span>