---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: ApproximateInputEncoder 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 67ef7a47a2e036f0953d946b4ace0e6673b173bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92720536"
---
# <a name="approximateinputencoder-function"></a><span data-ttu-id="7cb84-102">ApproximateInputEncoder 함수</span><span class="sxs-lookup"><span data-stu-id="7cb84-102">ApproximateInputEncoder function</span></span>

<span data-ttu-id="7cb84-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7cb84-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="7cb84-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7cb84-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7cb84-105">계수 및 허용 오차 집합이 지정 된 경우 지정 된 허용 오차를 기준으로 각 계수를 계산 기준 상태의 해당 진폭으로 준비 하는 상태 준비 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb84-105">Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.</span></span>

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a><span data-ttu-id="7cb84-106">입력</span><span class="sxs-lookup"><span data-stu-id="7cb84-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="7cb84-107">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7cb84-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7cb84-108">지정 된 계수를 입력 상태로 인코딩할 때 사용 되는 근사값입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb84-108">The approximation tolerance to be used in encoding the given coefficients into an input state.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="7cb84-109">계수: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="7cb84-109">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="7cb84-110">입력 상태로 인코딩될 계수입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb84-110">The coefficients to be encoded into an input state.</span></span>



## <a name="output--stategenerator"></a><span data-ttu-id="7cb84-111">출력: [Stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="7cb84-111">Output : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="7cb84-112">지정 된 레지스터에서 지정 된 계수를 입력 상태로 준비 하는 상태 준비 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb84-112">A state preparation operation that prepares the given coefficients as an input state on a given register.</span></span>