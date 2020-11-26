---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: DrawRandomBool 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192964"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="84068-102">DrawRandomBool 작업</span><span class="sxs-lookup"><span data-stu-id="84068-102">DrawRandomBool operation</span></span>

<span data-ttu-id="84068-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="84068-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="84068-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="84068-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="84068-105">성공 확률이 지정 된 경우 지정 된 확률을 사용 하 여 true 인 단일 베르누이 평가판을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="84068-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="84068-106">입력</span><span class="sxs-lookup"><span data-stu-id="84068-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="84068-107">successProbability: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="84068-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="84068-108">이 반환 되어야 하는 확률 `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="84068-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="84068-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="84068-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="84068-110">`true` 확률 `successProbability` 및 확률을 포함 `false` `1.0 - successProbability` 합니다.</span><span class="sxs-lookup"><span data-stu-id="84068-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>