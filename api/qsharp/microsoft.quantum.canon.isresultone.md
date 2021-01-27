---
uid: Microsoft.Quantum.Canon.IsResultOne
title: IsResultOne 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IsResultOne
qsharp.summary: Tests if a given Result value is equal to `One`.
ms.openlocfilehash: f259c21e6cc0a4886332e9ffcb546e527ec7def1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840322"
---
# <a name="isresultone-function"></a><span data-ttu-id="210d1-102">IsResultOne 함수</span><span class="sxs-lookup"><span data-stu-id="210d1-102">IsResultOne function</span></span>

<span data-ttu-id="210d1-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="210d1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="210d1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="210d1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="210d1-105">지정 된 결과 값이와 같은지 테스트 `One` 합니다.</span><span class="sxs-lookup"><span data-stu-id="210d1-105">Tests if a given Result value is equal to `One`.</span></span>

```qsharp
function IsResultOne (input : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="210d1-106">입력</span><span class="sxs-lookup"><span data-stu-id="210d1-106">Input</span></span>

### <a name="input--__invalidresult__"></a><span data-ttu-id="210d1-107">입력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="210d1-107">input : __invalid<Result>__</span></span>

<span data-ttu-id="210d1-108">`Result` 테스트할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="210d1-108">`Result` value to be tested.</span></span>



## <a name="output--bool"></a><span data-ttu-id="210d1-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="210d1-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="210d1-110">`true` `input` 가와 같으면를 반환 `One` 합니다.</span><span class="sxs-lookup"><span data-stu-id="210d1-110">Returns `true` if `input` is equal to `One`.</span></span>