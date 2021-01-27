---
uid: Microsoft.Quantum.Synthesis.RMEncoding
title: R 코딩 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: RMEncoding
qsharp.summary: '{-1,1} coding of a Boolean truth value'
ms.openlocfilehash: f3c54d2e40511dacb21618b4eaf1eef9f4903f9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855337"
---
# <a name="rmencoding-function"></a><span data-ttu-id="dfb34-102">R 코딩 함수</span><span class="sxs-lookup"><span data-stu-id="dfb34-102">RMEncoding function</span></span>

<span data-ttu-id="dfb34-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="dfb34-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="dfb34-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dfb34-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dfb34-105">{-1,1} 부울 값 코딩</span><span class="sxs-lookup"><span data-stu-id="dfb34-105">{-1,1} coding of a Boolean truth value</span></span>

```qsharp
function RMEncoding (b : Bool) : Int
```


## <a name="input"></a><span data-ttu-id="dfb34-106">입력</span><span class="sxs-lookup"><span data-stu-id="dfb34-106">Input</span></span>

### <a name="b--bool"></a><span data-ttu-id="dfb34-107">b: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dfb34-107">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dfb34-108">부울 값</span><span class="sxs-lookup"><span data-stu-id="dfb34-108">Boolean value</span></span>



## <a name="output--int"></a><span data-ttu-id="dfb34-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dfb34-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dfb34-110">가 false 이면 1이 고, `b` 그렇지 않으면-1입니다.</span><span class="sxs-lookup"><span data-stu-id="dfb34-110">1, if `b` is false, otherwise -1</span></span>