---
uid: Microsoft.Quantum.Random.DrawRandomPauli
title: DrawRandomPauli 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomPauli
qsharp.summary: Draws a random Pauli value.
ms.openlocfilehash: 9933fd4a9f04f7f08eaffa799ae77c8d60715386
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210134"
---
# <a name="drawrandompauli-operation"></a><span data-ttu-id="060fa-102">DrawRandomPauli 작업</span><span class="sxs-lookup"><span data-stu-id="060fa-102">DrawRandomPauli operation</span></span>

<span data-ttu-id="060fa-103">네임 스페이스: [Microsoft 양자. 무작위](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="060fa-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="060fa-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="060fa-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="060fa-105">임의의 Pauli 값을 그립니다.</span><span class="sxs-lookup"><span data-stu-id="060fa-105">Draws a random Pauli value.</span></span>

```qsharp
operation DrawRandomPauli () : Pauli
```


## <a name="output--pauli"></a><span data-ttu-id="060fa-106">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="060fa-106">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="060fa-107">`PauliI` `PauliX` `PauliY` 확률이 동일한,, 또는 `PauliZ` 입니다.</span><span class="sxs-lookup"><span data-stu-id="060fa-107">Either `PauliI`, `PauliX`, `PauliY`, or `PauliZ` with equal probability.</span></span>