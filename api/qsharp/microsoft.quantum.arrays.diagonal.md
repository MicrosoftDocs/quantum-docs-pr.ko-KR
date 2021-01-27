---
uid: Microsoft.Quantum.Arrays.Diagonal
title: 대각선 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 2857046f59a958fed106af0944b75baaa3292e96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842822"
---
# <a name="diagonal-function"></a><span data-ttu-id="2d100-102">대각선 함수</span><span class="sxs-lookup"><span data-stu-id="2d100-102">Diagonal function</span></span>

<span data-ttu-id="2d100-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2d100-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2d100-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2d100-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2d100-105">2 차원 배열의 대각선 요소 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d100-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="2d100-106">설명</span><span class="sxs-lookup"><span data-stu-id="2d100-106">Description</span></span>

<span data-ttu-id="2d100-107">2 차원 배열에 정사각형이 아닌 도형이 있으면 행 및 열 수에 대 한 최소의 대각선이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d100-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="2d100-108">입력</span><span class="sxs-lookup"><span data-stu-id="2d100-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="2d100-109">matrix: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="2d100-109">matrix : 'T[][]</span></span>

<span data-ttu-id="2d100-110">2 차원 행렬 (행 단위 순서)</span><span class="sxs-lookup"><span data-stu-id="2d100-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="2d100-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="2d100-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2d100-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2d100-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2d100-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="2d100-113">'T</span></span>

<span data-ttu-id="2d100-114">에 있는 각 요소의 형식입니다 `matrix` .</span><span class="sxs-lookup"><span data-stu-id="2d100-114">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="2d100-115">예제</span><span class="sxs-lookup"><span data-stu-id="2d100-115">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let diagonal = Diagonal(matrix);
// same as: column = [1, 5, 9]
```

## <a name="see-also"></a><span data-ttu-id="2d100-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2d100-116">See Also</span></span>

- [<span data-ttu-id="2d100-117">Microsoft 양자 배열</span><span class="sxs-lookup"><span data-stu-id="2d100-117">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)