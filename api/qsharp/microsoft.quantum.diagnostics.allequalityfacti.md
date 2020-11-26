---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: AllEqualityFactI 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: 92b57f49407d558e5f8d0365c168b7890f1f4981
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223887"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="268db-102">AllEqualityFactI 함수</span><span class="sxs-lookup"><span data-stu-id="268db-102">AllEqualityFactI function</span></span>

<span data-ttu-id="268db-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="268db-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="268db-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="268db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="268db-105">두 정수 값 배열이 동일한 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="268db-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="268db-106">입력</span><span class="sxs-lookup"><span data-stu-id="268db-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="268db-107">actual: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="268db-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="268db-108">관련 테스트 사례에 의해 생성 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="268db-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="268db-109">예상: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="268db-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="268db-110">관련 테스트 사례에서 예상 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="268db-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="268db-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="268db-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="268db-112">배열이 같지 않으면 인쇄할 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="268db-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="268db-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="268db-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

