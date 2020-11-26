---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: ColumnAtUnchecked 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 06fce23bbf7142ee0e0b0ed3f2c0578676f2097b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221592"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="1101b-102">ColumnAtUnchecked 함수</span><span class="sxs-lookup"><span data-stu-id="1101b-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="1101b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1101b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1101b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1101b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1101b-105">이 함수는 행렬 셰이프를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1101b-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="1101b-106">Description</span><span class="sxs-lookup"><span data-stu-id="1101b-106">Description</span></span>

<span data-ttu-id="1101b-107">이 함수는 유효한 사각형 모양의 입력 행렬을 이미 확인 하는 다른 다차원 함수에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1101b-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="1101b-108">입력</span><span class="sxs-lookup"><span data-stu-id="1101b-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="1101b-109">열: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1101b-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="1101b-110">matrix: ' t [] []</span><span class="sxs-lookup"><span data-stu-id="1101b-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="1101b-111">출력: ' t []</span><span class="sxs-lookup"><span data-stu-id="1101b-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1101b-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1101b-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1101b-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="1101b-113">'T</span></span>

