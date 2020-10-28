---
uid: Microsoft.Quantum.Canon.IsResultOne
title: IsResultOne 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IsResultOne
qsharp.summary: Tests if a given Result value is equal to `One`.
ms.openlocfilehash: fa8845fd92e5c16b4ff15436caf42df4f1e151cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716052"
---
# <a name="isresultone-function"></a><span data-ttu-id="d0a5e-102">IsResultOne 함수</span><span class="sxs-lookup"><span data-stu-id="d0a5e-102">IsResultOne function</span></span>

<span data-ttu-id="d0a5e-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d0a5e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d0a5e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0a5e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0a5e-105">지정 된 결과 값이와 같은지 테스트 `One` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a5e-105">Tests if a given Result value is equal to `One`.</span></span>

```qsharp
function IsResultOne (input : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="d0a5e-106">입력</span><span class="sxs-lookup"><span data-stu-id="d0a5e-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="d0a5e-107">입력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="d0a5e-107">input : __invalid<Result>__</span></span>

<span data-ttu-id="d0a5e-108">`Result` 테스트할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d0a5e-108">`Result` value to be tested.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d0a5e-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d0a5e-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d0a5e-110">`true` `input` 가와 같으면를 반환 `One` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a5e-110">Returns `true` if `input` is equal to `One`.</span></span>