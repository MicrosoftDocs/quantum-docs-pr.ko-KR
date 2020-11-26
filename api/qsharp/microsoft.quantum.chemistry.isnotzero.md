---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: IsNotZero 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: f80dbba6a51e62970e87c2782faba558340d2bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204065"
---
# <a name="isnotzero-function"></a><span data-ttu-id="aa0cc-102">IsNotZero 함수</span><span class="sxs-lookup"><span data-stu-id="aa0cc-102">IsNotZero function</span></span>

<span data-ttu-id="aa0cc-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="aa0cc-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="aa0cc-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="aa0cc-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="aa0cc-105">`Double`숫자가 약 0이 아닌지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-105">Checks whether a `Double` number is not approximately zero.</span></span>

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="aa0cc-106">입력</span><span class="sxs-lookup"><span data-stu-id="aa0cc-106">Input</span></span>

### <a name="number--double"></a><span data-ttu-id="aa0cc-107">숫자: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="aa0cc-107">number : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="aa0cc-108">확인할 수</span><span class="sxs-lookup"><span data-stu-id="aa0cc-108">Number to be checked</span></span>



## <a name="output--bool"></a><span data-ttu-id="aa0cc-109">출력: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="aa0cc-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="aa0cc-110">`number`에 보다 큰 절대값 값이 있으면 true를 반환 `1e-15` 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-110">Returns true if `number` has an absolute value greater than `1e-15`.</span></span>