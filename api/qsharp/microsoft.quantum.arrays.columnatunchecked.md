---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: ColumnAtUnchecked 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 17211c1ae1fe12fcadf34a9411f9b0cf0cdcab50
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719449"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="59315-102">ColumnAtUnchecked 함수</span><span class="sxs-lookup"><span data-stu-id="59315-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="59315-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="59315-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="59315-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59315-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59315-105">이 함수는 행렬 셰이프를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59315-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="59315-106">Description</span><span class="sxs-lookup"><span data-stu-id="59315-106">Description</span></span>

<span data-ttu-id="59315-107">이 함수는 유효한 사각형 모양의 입력 행렬을 이미 확인 하는 다른 다차원 함수에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59315-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="59315-108">입력</span><span class="sxs-lookup"><span data-stu-id="59315-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="59315-109">열: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="59315-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="59315-110">matrix: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="59315-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="59315-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="59315-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="59315-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="59315-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="59315-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="59315-113">'T</span></span>

