---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: InputEncoder 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: 771cf01866498f4662864939e6946526c2b5827a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709752"
---
# <a name="inputencoder-function"></a><span data-ttu-id="28049-102">InputEncoder 함수</span><span class="sxs-lookup"><span data-stu-id="28049-102">InputEncoder function</span></span>

<span data-ttu-id="28049-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="28049-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="28049-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="28049-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="28049-105">계수 및 허용 오차 집합이 지정 된 경우 각 계수를 계산 기준 상태의 해당 진폭으로 준비 하는 상태 준비 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28049-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.</span></span>

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="28049-106">입력</span><span class="sxs-lookup"><span data-stu-id="28049-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="28049-107">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="28049-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="28049-108">입력 상태로 인코딩될 계수입니다.</span><span class="sxs-lookup"><span data-stu-id="28049-108">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="28049-109">출력: [Stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="28049-109">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="28049-110">지정 된 레지스터에서 지정 된 계수를 입력 상태로 준비 하는 상태 준비 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="28049-110">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>