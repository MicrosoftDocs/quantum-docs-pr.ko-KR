---
uid: Microsoft.Quantum.Convert.ResultAsBool
title: ResultAsBool 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: ResultAsBool
qsharp.summary: Converts a `Result` type to a `Bool` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.
ms.openlocfilehash: 9de7ca64992e0a4d73c1d00218b3eab4ab545a1e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98832556"
---
# <a name="resultasbool-function"></a><span data-ttu-id="ac787-102">ResultAsBool 함수</span><span class="sxs-lookup"><span data-stu-id="ac787-102">ResultAsBool function</span></span>

<span data-ttu-id="ac787-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="ac787-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="ac787-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac787-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ac787-105">`Result`형식을 형식으로 변환 `Bool` `One` 합니다. 여기서은로 매핑되고는 `true` `Zero` 에 매핑됩니다 `false` .</span><span class="sxs-lookup"><span data-stu-id="ac787-105">Converts a `Result` type to a `Bool` type, where `One` is mapped to `true` and `Zero` is mapped to `false`.</span></span>

```qsharp
function ResultAsBool (input : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="ac787-106">입력</span><span class="sxs-lookup"><span data-stu-id="ac787-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="ac787-107">입력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="ac787-107">input : __invalid<Result>__</span></span>

<span data-ttu-id="ac787-108">`Result` 변환 될입니다.</span><span class="sxs-lookup"><span data-stu-id="ac787-108">`Result` to be converted.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ac787-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ac787-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ac787-110">`input`를 나타내는 `Bool`입니다.</span><span class="sxs-lookup"><span data-stu-id="ac787-110">A `Bool` representing the `input`.</span></span>