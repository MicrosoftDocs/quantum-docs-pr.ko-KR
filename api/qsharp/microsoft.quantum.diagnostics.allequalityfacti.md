---
uid: Microsoft.Quantum.Diagnostics.AllEqualityFactI
title: AllEqualityFactI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllEqualityFactI
qsharp.summary: Asserts that two arrays of integer values are equal.
ms.openlocfilehash: 9ccd212010ae557de5ca4ab2a38d4724c5c29aa8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713070"
---
# <a name="allequalityfacti-function"></a><span data-ttu-id="8fc12-102">AllEqualityFactI 함수</span><span class="sxs-lookup"><span data-stu-id="8fc12-102">AllEqualityFactI function</span></span>

<span data-ttu-id="8fc12-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="8fc12-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="8fc12-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8fc12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8fc12-105">두 정수 값 배열이 동일한 것을 어설션 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fc12-105">Asserts that two arrays of integer values are equal.</span></span>

```qsharp
function AllEqualityFactI (actual : Int[], expected : Int[], message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="8fc12-106">입력</span><span class="sxs-lookup"><span data-stu-id="8fc12-106">Input</span></span>

### <a name="actual--int"></a><span data-ttu-id="8fc12-107">actual: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8fc12-107">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8fc12-108">관련 테스트 사례에 의해 생성 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8fc12-108">The array that is produced by a test case of interest.</span></span>


### <a name="expected--int"></a><span data-ttu-id="8fc12-109">예상: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8fc12-109">expected : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8fc12-110">관련 테스트 사례에서 예상 되는 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8fc12-110">The array that is expected from a test case of interest.</span></span>


### <a name="message--string"></a><span data-ttu-id="8fc12-111">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="8fc12-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="8fc12-112">배열이 같지 않으면 인쇄할 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="8fc12-112">A message to be printed if the arrays are not equal.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8fc12-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8fc12-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

