---
uid: Microsoft.Quantum.Canon.GrayCode
title: GrayCode 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206887"
---
# <a name="graycode-function"></a><span data-ttu-id="1d618-102">GrayCode 함수</span><span class="sxs-lookup"><span data-stu-id="1d618-102">GrayCode function</span></span>

<span data-ttu-id="1d618-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1d618-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1d618-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d618-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d618-105">회색 코드 시퀀스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d618-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="1d618-106">입력</span><span class="sxs-lookup"><span data-stu-id="1d618-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="1d618-107">n: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1d618-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1d618-108">비트 수</span><span class="sxs-lookup"><span data-stu-id="1d618-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="1d618-109">Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="1d618-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="1d618-110">튜플 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1d618-110">Array of tuples.</span></span> <span data-ttu-id="1d618-111">튜플의 첫 번째 값은 GrayCode의 값입니다. 튜플의 값은 현재 값에서 변경 하 여 다음 항목을 가져오기 위한 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1d618-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>