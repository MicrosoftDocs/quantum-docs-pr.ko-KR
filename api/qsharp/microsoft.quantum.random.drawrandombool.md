---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: DrawRandomBool 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720277"
---
# <a name="drawrandombool-operation"></a><span data-ttu-id="4ae37-102">DrawRandomBool 작업</span><span class="sxs-lookup"><span data-stu-id="4ae37-102">DrawRandomBool operation</span></span>

<span data-ttu-id="4ae37-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="4ae37-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="4ae37-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4ae37-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4ae37-105">성공 확률이 지정 된 경우 지정 된 확률을 사용 하 여 true 인 단일 베르누이 평가판을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae37-105">Given a success probability, returns a single Bernoulli trial that is true with the given probability.</span></span>

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="4ae37-106">입력</span><span class="sxs-lookup"><span data-stu-id="4ae37-106">Input</span></span>

### <a name="successprobability--double"></a><span data-ttu-id="4ae37-107">successProbability: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4ae37-107">successProbability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4ae37-108">이 반환 되어야 하는 확률 `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae37-108">The probability with which `true` should be returned.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4ae37-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4ae37-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4ae37-110">`true` 확률 `successProbability` 및 확률을 포함 `false` `1.0 - successProbability` 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae37-110">`true` with probability `successProbability` and `false` with probability `1.0 - successProbability`.</span></span>