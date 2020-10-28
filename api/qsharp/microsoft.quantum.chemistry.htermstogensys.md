---
uid: Microsoft.Quantum.Chemistry.HTermsToGenSys
title: HTermsToGenSys 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenSys
qsharp.summary: Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.
ms.openlocfilehash: b78ff393fa1e51c38028ef56bb3c61b8f1d5e478
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714841"
---
# <a name="htermstogensys-function"></a><span data-ttu-id="f0179-102">HTermsToGenSys 함수</span><span class="sxs-lookup"><span data-stu-id="f0179-102">HTermsToGenSys function</span></span>

<span data-ttu-id="f0179-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f0179-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="f0179-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0179-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0179-105">Hamiltonian `HTerm[]` 데이터 형식을 GeneratorSystem로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0179-105">Converts a Hamiltonian in `HTerm[]` data format to a GeneratorSystem.</span></span>

```qsharp
function HTermsToGenSys (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="f0179-106">입력</span><span class="sxs-lookup"><span data-stu-id="f0179-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="f0179-107">데이터: [Hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="f0179-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="f0179-108">형식의 입력 데이터 `HTerm[]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f0179-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="f0179-109">termType: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f0179-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f0179-110">추가 정보를 GeneratorIndex에 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f0179-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="f0179-111">출력: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="f0179-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="f0179-112">입력이 나타내는 Hamiltonian를 나타내는 GeneratorSystem `data` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f0179-112">A GeneratorSystem representing a Hamiltonian represented by the input `data`.</span></span>