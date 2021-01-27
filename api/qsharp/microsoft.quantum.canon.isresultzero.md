---
uid: Microsoft.Quantum.Canon.IsResultZero
title: IsResultZero 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IsResultZero
qsharp.summary: Tests if a given Result value is equal to `Zero`.
ms.openlocfilehash: b1e7cf6324a2a90f10b6aa93811f2df60fe3afbd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840309"
---
# <a name="isresultzero-function"></a><span data-ttu-id="50356-102">IsResultZero 함수</span><span class="sxs-lookup"><span data-stu-id="50356-102">IsResultZero function</span></span>

<span data-ttu-id="50356-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="50356-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="50356-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="50356-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="50356-105">지정 된 결과 값이와 같은지 테스트 `Zero` 합니다.</span><span class="sxs-lookup"><span data-stu-id="50356-105">Tests if a given Result value is equal to `Zero`.</span></span>

```qsharp
function IsResultZero (input : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="50356-106">입력</span><span class="sxs-lookup"><span data-stu-id="50356-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="50356-107">입력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="50356-107">input : __invalid<Result>__</span></span>

<span data-ttu-id="50356-108">`Result` 테스트할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="50356-108">`Result` value to be tested.</span></span>



## <a name="output--bool"></a><span data-ttu-id="50356-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="50356-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="50356-110">`true` `input` 가와 같으면를 반환 `Zero` 합니다.</span><span class="sxs-lookup"><span data-stu-id="50356-110">Returns `true` if `input` is equal to `Zero`.</span></span>