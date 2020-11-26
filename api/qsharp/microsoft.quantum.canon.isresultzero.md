---
uid: Microsoft.Quantum.Canon.IsResultZero
title: IsResultZero 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IsResultZero
qsharp.summary: Tests if a given Result value is equal to `Zero`.
ms.openlocfilehash: b4e9b62b20e12a8dce544ce16dcddcf15fdf2680
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206530"
---
# <a name="isresultzero-function"></a><span data-ttu-id="9b37b-102">IsResultZero 함수</span><span class="sxs-lookup"><span data-stu-id="9b37b-102">IsResultZero function</span></span>

<span data-ttu-id="9b37b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9b37b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9b37b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b37b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b37b-105">지정 된 결과 값이와 같은지 테스트 `Zero` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b37b-105">Tests if a given Result value is equal to `Zero`.</span></span>

```qsharp
function IsResultZero (input : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="9b37b-106">입력</span><span class="sxs-lookup"><span data-stu-id="9b37b-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="9b37b-107">입력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="9b37b-107">input : __invalid<Result>__</span></span>

<span data-ttu-id="9b37b-108">`Result` 테스트할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9b37b-108">`Result` value to be tested.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9b37b-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9b37b-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9b37b-110">`true` `input` 가와 같으면를 반환 `Zero` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b37b-110">Returns `true` if `input` is equal to `Zero`.</span></span>