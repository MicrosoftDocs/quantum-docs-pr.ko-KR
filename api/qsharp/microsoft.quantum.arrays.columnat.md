---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: ColumnAt 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 32dc814de9b04563c2798a768f121723a1a8252c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846266"
---
# <a name="columnat-function"></a><span data-ttu-id="cc268-102">ColumnAt 함수</span><span class="sxs-lookup"><span data-stu-id="cc268-102">ColumnAt function</span></span>

<span data-ttu-id="cc268-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cc268-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cc268-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc268-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc268-105">행렬에서 열을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc268-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="cc268-106">설명</span><span class="sxs-lookup"><span data-stu-id="cc268-106">Description</span></span>

<span data-ttu-id="cc268-107">이 함수는 행 단위 순서로 행렬의 열을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc268-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="cc268-108">Corrsponds 행을 추출 하면 첫 번째 인덱스의 요소에 액세스할 수 있으므로 추가 처리가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc268-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="cc268-109">입력</span><span class="sxs-lookup"><span data-stu-id="cc268-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="cc268-110">열: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cc268-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cc268-111">행렬의 열</span><span class="sxs-lookup"><span data-stu-id="cc268-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="cc268-112">matrix: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="cc268-112">matrix : 'T[][]</span></span>

<span data-ttu-id="cc268-113">2 차원 행렬 (행 단위 순서)</span><span class="sxs-lookup"><span data-stu-id="cc268-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="cc268-114">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="cc268-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cc268-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cc268-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cc268-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="cc268-116">'T</span></span>

<span data-ttu-id="cc268-117">에 있는 각 요소의 형식입니다 `matrix` .</span><span class="sxs-lookup"><span data-stu-id="cc268-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="cc268-118">예제</span><span class="sxs-lookup"><span data-stu-id="cc268-118">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let column = ColumnAt(0, matrix);
// same as: column = [1, 4, 7]
```

## <a name="see-also"></a><span data-ttu-id="cc268-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cc268-119">See Also</span></span>

- [<span data-ttu-id="cc268-120">Microsoft 양자 배열</span><span class="sxs-lookup"><span data-stu-id="cc268-120">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="cc268-121">Microsoft 양자. 배열 대각선</span><span class="sxs-lookup"><span data-stu-id="cc268-121">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)