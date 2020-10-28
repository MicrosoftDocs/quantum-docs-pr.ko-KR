---
uid: Microsoft.Quantum.Canon.IsResultZero
title: IsResultZero 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IsResultZero
qsharp.summary: Tests if a given Result value is equal to `Zero`.
ms.openlocfilehash: 790551690cfba42df4cf7aa77e53e303050bdf39
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716031"
---
# <a name="isresultzero-function"></a><span data-ttu-id="f6a14-102">IsResultZero 함수</span><span class="sxs-lookup"><span data-stu-id="f6a14-102">IsResultZero function</span></span>

<span data-ttu-id="f6a14-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f6a14-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f6a14-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f6a14-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f6a14-105">지정 된 결과 값이와 같은지 테스트 `Zero` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a14-105">Tests if a given Result value is equal to `Zero`.</span></span>

```qsharp
function IsResultZero (input : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="f6a14-106">입력</span><span class="sxs-lookup"><span data-stu-id="f6a14-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="f6a14-107">입력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="f6a14-107">input : __invalid<Result>__</span></span>

<span data-ttu-id="f6a14-108">`Result` 테스트할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f6a14-108">`Result` value to be tested.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f6a14-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f6a14-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f6a14-110">`true` `input` 가와 같으면를 반환 `Zero` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a14-110">Returns `true` if `input` is equal to `Zero`.</span></span>