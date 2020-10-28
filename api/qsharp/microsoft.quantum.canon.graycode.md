---
uid: Microsoft.Quantum.Canon.GrayCode
title: GrayCode 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716164"
---
# <a name="graycode-function"></a><span data-ttu-id="60428-102">GrayCode 함수</span><span class="sxs-lookup"><span data-stu-id="60428-102">GrayCode function</span></span>

<span data-ttu-id="60428-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="60428-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="60428-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="60428-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="60428-105">회색 코드 시퀀스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60428-105">Creates Gray code sequences</span></span>

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="60428-106">입력</span><span class="sxs-lookup"><span data-stu-id="60428-106">Input</span></span>

### <a name="n--int"></a><span data-ttu-id="60428-107">n: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60428-107">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="60428-108">비트 수</span><span class="sxs-lookup"><span data-stu-id="60428-108">Number of bits</span></span>



## <a name="output--intint"></a><span data-ttu-id="60428-109">Output: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="60428-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="60428-110">튜플 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="60428-110">Array of tuples.</span></span> <span data-ttu-id="60428-111">튜플의 첫 번째 값은 GrayCode의 값입니다. 튜플의 값은 현재 값에서 변경 하 여 다음 항목을 가져오기 위한 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="60428-111">First value in tuple is value in GrayCode sequence Second value in tuple is position to change in current value to get next one.</span></span>