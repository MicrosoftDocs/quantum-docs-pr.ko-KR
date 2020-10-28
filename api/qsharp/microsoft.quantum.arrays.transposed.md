---
uid: Microsoft.Quantum.Arrays.Transposed
title: 전치 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 54071c461cf9f9411c332763b81e3bc448fb6c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718813"
---
# <a name="transposed-function"></a><span data-ttu-id="7d5d9-102">전치 함수</span><span class="sxs-lookup"><span data-stu-id="7d5d9-102">Transposed function</span></span>

<span data-ttu-id="7d5d9-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7d5d9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7d5d9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7d5d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7d5d9-105">배열의 배열로 표시 되는 매트릭스의 바꾸기를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5d9-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="7d5d9-106">Description</span><span class="sxs-lookup"><span data-stu-id="7d5d9-106">Description</span></span>

<span data-ttu-id="7d5d9-107">$R $ rows 및 $c $ columns를 사용 하 여 $r \times c $ matrix로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5d9-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="7d5d9-108">행렬은 행 기반입니다. 즉, `matrix[i][j]` 행 $i $ 및 열 $j $의 요소에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5d9-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="7d5d9-109">이 함수는 입력 행렬의 전치 인 $c \times r $ matrix를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5d9-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="7d5d9-110">입력</span><span class="sxs-lookup"><span data-stu-id="7d5d9-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="7d5d9-111">matrix: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="7d5d9-111">matrix : 'T[][]</span></span>

<span data-ttu-id="7d5d9-112">행 기반 $r \times c $ 행렬</span><span class="sxs-lookup"><span data-stu-id="7d5d9-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="7d5d9-113">출력: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="7d5d9-113">Output : 'T[][]</span></span>

<span data-ttu-id="7d5d9-114">$C \times r $ matrix로 바뀜</span><span class="sxs-lookup"><span data-stu-id="7d5d9-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7d5d9-115">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d5d9-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7d5d9-116">없습니다</span><span class="sxs-lookup"><span data-stu-id="7d5d9-116">'T</span></span>

<span data-ttu-id="7d5d9-117">에 있는 각 요소의 형식입니다 `matrix` .</span><span class="sxs-lookup"><span data-stu-id="7d5d9-117">The type of each element of `matrix`.</span></span>