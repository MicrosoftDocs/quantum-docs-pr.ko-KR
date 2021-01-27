---
uid: Microsoft.Quantum.Arrays.Transposed
title: 전치 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 913f1829ef53ec3eb6944be8b8e3eb37b431f27e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850929"
---
# <a name="transposed-function"></a><span data-ttu-id="aa5f7-102">전치 함수</span><span class="sxs-lookup"><span data-stu-id="aa5f7-102">Transposed function</span></span>

<span data-ttu-id="aa5f7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aa5f7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aa5f7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa5f7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa5f7-105">배열의 배열로 표시 되는 매트릭스의 바꾸기를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="aa5f7-106">설명</span><span class="sxs-lookup"><span data-stu-id="aa5f7-106">Description</span></span>

<span data-ttu-id="aa5f7-107">$R $ rows 및 $c $ columns를 사용 하 여 $r \times c $ matrix로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="aa5f7-108">행렬은 행 기반입니다. 즉, `matrix[i][j]` 행 $i $ 및 열 $j $의 요소에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="aa5f7-109">이 함수는 입력 행렬의 전치 인 $c \times r $ matrix를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="aa5f7-110">입력</span><span class="sxs-lookup"><span data-stu-id="aa5f7-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="aa5f7-111">matrix: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="aa5f7-111">matrix : 'T[][]</span></span>

<span data-ttu-id="aa5f7-112">행 기반 $r \times c $ 행렬</span><span class="sxs-lookup"><span data-stu-id="aa5f7-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="aa5f7-113">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="aa5f7-113">Output : 'T[][]</span></span>

<span data-ttu-id="aa5f7-114">$C \times r $ matrix로 바뀜</span><span class="sxs-lookup"><span data-stu-id="aa5f7-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="aa5f7-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa5f7-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aa5f7-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="aa5f7-116">'T</span></span>

<span data-ttu-id="aa5f7-117">에 있는 각 요소의 형식입니다 `matrix` .</span><span class="sxs-lookup"><span data-stu-id="aa5f7-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="aa5f7-118">예제</span><span class="sxs-lookup"><span data-stu-id="aa5f7-118">Example</span></span>

```qsharp
// same as [[1, 4], [2, 5], [3, 6]]
let transposed = Transposed([[1, 2, 3], [4, 5, 6]]);
```