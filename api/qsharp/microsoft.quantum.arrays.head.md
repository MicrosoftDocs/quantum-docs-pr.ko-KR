---
uid: Microsoft.Quantum.Arrays.Head
title: Head 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 6dd181914b5ed3ef16a02b31cb6131daf2a34e19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848563"
---
# <a name="head-function"></a><span data-ttu-id="2c162-102">Head 함수</span><span class="sxs-lookup"><span data-stu-id="2c162-102">Head function</span></span>

<span data-ttu-id="2c162-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2c162-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2c162-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c162-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c162-105">배열의 첫 번째 요소를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c162-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="2c162-106">입력</span><span class="sxs-lookup"><span data-stu-id="2c162-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="2c162-107">array: ' A []</span><span class="sxs-lookup"><span data-stu-id="2c162-107">array : 'A[]</span></span>

<span data-ttu-id="2c162-108">첫 번째 요소를 가져올 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="2c162-108">Array of which the first element is taken.</span></span> <span data-ttu-id="2c162-109">배열의 길이는 1 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c162-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="2c162-110">출력: ' A</span><span class="sxs-lookup"><span data-stu-id="2c162-110">Output : 'A</span></span>

<span data-ttu-id="2c162-111">배열의 첫 번째 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="2c162-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2c162-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2c162-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="2c162-113">' A</span><span class="sxs-lookup"><span data-stu-id="2c162-113">'A</span></span>

<span data-ttu-id="2c162-114">배열 요소의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2c162-114">The type of the array elements.</span></span>