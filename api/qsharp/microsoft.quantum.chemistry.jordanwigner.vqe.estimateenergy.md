---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: EstimateEnergy 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713749"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="82697-102">EstimateEnergy 작업</span><span class="sxs-lookup"><span data-stu-id="82697-102">EstimateEnergy operation</span></span>

<span data-ttu-id="82697-103">네임 스페이스: [JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="82697-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="82697-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="82697-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="82697-105">개별 Jordan-Wigner 용어로 제공한 에너지를 합산 하 여 분자의 에너지를 추정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82697-105">Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.</span></span>

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="82697-106">Description</span><span class="sxs-lookup"><span data-stu-id="82697-106">Description</span></span>

<span data-ttu-id="82697-107">이 작업은 회전 up-down 인덱싱 규칙을 암시적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="82697-107">This operation implicitly relies on the spin up-down indexing convention.</span></span>

## <a name="input"></a><span data-ttu-id="82697-108">입력</span><span class="sxs-lookup"><span data-stu-id="82697-108">Input</span></span>

### <a name="jwhamiltonian--jordanwignerencodingdata"></a><span data-ttu-id="82697-109">jwHamiltonian: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="82697-109">jwHamiltonian : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="82697-110">Jordan-Wigner Hamiltonian입니다.</span><span class="sxs-lookup"><span data-stu-id="82697-110">The Jordan-Wigner Hamiltonian.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="82697-111">nSamples: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="82697-111">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="82697-112">용어 기대 예측에 사용할 샘플 수입니다.</span><span class="sxs-lookup"><span data-stu-id="82697-112">The number of samples to use for the estimation of the term expectations.</span></span>



## <a name="output--double"></a><span data-ttu-id="82697-113">출력: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="82697-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="82697-114">분자의 예상 에너지</span><span class="sxs-lookup"><span data-stu-id="82697-114">The estimated energy of the molecule</span></span>