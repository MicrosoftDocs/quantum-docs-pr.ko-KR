---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: SingleQubitProcessTomographyMeasurement 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 883b98ad4f2d0ac4a02e55e444c04e8e7cf37af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839647"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a><span data-ttu-id="180d3-102">SingleQubitProcessTomographyMeasurement 작업</span><span class="sxs-lookup"><span data-stu-id="180d3-102">SingleQubitProcessTomographyMeasurement operation</span></span>

<span data-ttu-id="180d3-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="180d3-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="180d3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="180d3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="180d3-105">특정 채널을 지정 하 여 Pauli에서 단일 tomography 비트 프로세스를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="180d3-105">Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.</span></span>

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a><span data-ttu-id="180d3-106">입력</span><span class="sxs-lookup"><span data-stu-id="180d3-106">Input</span></span>

### <a name="preparation--pauli"></a><span data-ttu-id="180d3-107">준비: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="180d3-107">preparation : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="180d3-108">Pabit를 준비할 수 있는 Pauli 기준 요소 $P입니다.</span><span class="sxs-lookup"><span data-stu-id="180d3-108">The Pauli basis element $P$ in which a qubit is to be prepared.</span></span>


### <a name="measurement--pauli"></a><span data-ttu-id="180d3-109">측정: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="180d3-109">measurement : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="180d3-110">이 요소는 원하는 비트를 측정할 수 있는 $Q $입니다.</span><span class="sxs-lookup"><span data-stu-id="180d3-110">The Pauli basis element $Q$ in which a qubit is to be measured.</span></span>


### <a name="channel--qubit--unit"></a><span data-ttu-id="180d3-111">채널:가 중 [비트](xref:microsoft.quantum.lang-ref.qubit) => [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="180d3-111">channel : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="180d3-112">Process tomography를 사용 하 여 동작을 예측 하는 단일 valbit channel $ \Lambda $.</span><span class="sxs-lookup"><span data-stu-id="180d3-112">A single qubit channel $\Lambda$ whose behavior is being estimated with process tomography.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="180d3-113">출력: __잘못 <Result> 됨__</span><span class="sxs-lookup"><span data-stu-id="180d3-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="180d3-114">`Zero`확률 $ $ \Begin{align} \Pr (\texttt{Zero} | \Pr;)이 포함 된 결과 P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).</span><span class="sxs-lookup"><span data-stu-id="180d3-114">The Result `Zero` with probability $$ \begin{align} \Pr(\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left( \frac{\boldone + Q}{2} \Lambda\left[ \frac{\boldone + P}{2} \right] \right).</span></span>
<span data-ttu-id="180d3-115">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="180d3-115">\end{align} $$</span></span>

## <a name="remarks"></a><span data-ttu-id="180d3-116">설명</span><span class="sxs-lookup"><span data-stu-id="180d3-116">Remarks</span></span>

<span data-ttu-id="180d3-117">이 작업에서 반환 되는 결과에 대 한 분포는 2 ~ 2-tomography의 특별 한 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="180d3-117">The distribution over results returned by this operation is a special case of two-qubit state tomography.</span></span> <span data-ttu-id="180d3-118">$ \Rho = J (\Lambda)/$2는 $ \Lambda $의 Choi – Jamiłkowski state입니다.</span><span class="sxs-lookup"><span data-stu-id="180d3-118">Let $\rho = J(\Lambda) / 2$ be the Choi–Jamiłkowski state for $\Lambda$.</span></span> <span data-ttu-id="180d3-119">그런 다음 위의 분포가 $ $ \begin{align} \Pr (\texttt{Zero} | \rho;)과 동일 합니다. M) = \operatorname{Tr} (M \rho), \end{align} $ $ where $M = 2 (\boldone + P) ^ \mathrm{T}/2\cdot (\boldone + Q)/$2는 $P $ 및 $Q $에 해당 하는 유효 측정입니다.</span><span class="sxs-lookup"><span data-stu-id="180d3-119">Then, the distribution above is identical to $$ \begin{align} \Pr(\texttt{Zero} | \rho; M) = \operatorname{Tr}(M \rho), \end{align} $$ where $M = 2 (\boldone + P)^\mathrm{T} / 2 \cdot (\boldone + Q) / 2$ is the effective measurement corresponding to $P$ and $Q$.</span></span>