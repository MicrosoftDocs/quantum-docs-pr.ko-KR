---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: ColumnAt 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719456"
---
# <a name="columnat-function"></a><span data-ttu-id="51902-102">ColumnAt 함수</span><span class="sxs-lookup"><span data-stu-id="51902-102">ColumnAt function</span></span>

<span data-ttu-id="51902-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="51902-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="51902-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51902-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51902-105">행렬에서 열을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="51902-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="51902-106">Description</span><span class="sxs-lookup"><span data-stu-id="51902-106">Description</span></span>

<span data-ttu-id="51902-107">이 함수는 행 단위 순서로 행렬의 열을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="51902-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="51902-108">Corrsponds 행을 추출 하면 첫 번째 인덱스의 요소에 액세스할 수 있으므로 추가 처리가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51902-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="51902-109">입력</span><span class="sxs-lookup"><span data-stu-id="51902-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="51902-110">열: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51902-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51902-111">행렬의 열</span><span class="sxs-lookup"><span data-stu-id="51902-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="51902-112">matrix: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="51902-112">matrix : 'T[][]</span></span>

<span data-ttu-id="51902-113">2 차원 행렬 (행 단위 순서)</span><span class="sxs-lookup"><span data-stu-id="51902-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="51902-114">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="51902-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="51902-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="51902-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="51902-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="51902-116">'T</span></span>

<span data-ttu-id="51902-117">에 있는 각 요소의 형식입니다 `matrix` .</span><span class="sxs-lookup"><span data-stu-id="51902-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="51902-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="51902-118">See Also</span></span>

- [<span data-ttu-id="51902-119">Microsoft 양자 배열</span><span class="sxs-lookup"><span data-stu-id="51902-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="51902-120">Microsoft 양자. 배열 대각선</span><span class="sxs-lookup"><span data-stu-id="51902-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)