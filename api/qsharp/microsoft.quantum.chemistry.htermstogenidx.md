---
uid: Microsoft.Quantum.Chemistry.HTermsToGenIdx
title: HTermsToGenIdx 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermsToGenIdx
qsharp.summary: Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.
ms.openlocfilehash: 73324a48cc4b42de0d5d8618ad9e833d289125f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714855"
---
# <a name="htermstogenidx-function"></a><span data-ttu-id="c34d7-102">HTermsToGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="c34d7-102">HTermsToGenIdx function</span></span>

<span data-ttu-id="c34d7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c34d7-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="c34d7-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c34d7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c34d7-105">인덱스를 데이터 형식의 Hamiltonian 용어로 변환 `HTerm[]` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c34d7-105">Converts an index to a Hamiltonian term in `HTerm[]` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermsToGenIdx (data : Microsoft.Quantum.Chemistry.HTerm[], termType : Int[], idx : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="c34d7-106">입력</span><span class="sxs-lookup"><span data-stu-id="c34d7-106">Input</span></span>

### <a name="data--hterm"></a><span data-ttu-id="c34d7-107">데이터: [Hterm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span><span class="sxs-lookup"><span data-stu-id="c34d7-107">data : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)[]</span></span>

<span data-ttu-id="c34d7-108">형식의 입력 데이터 `HTerm[]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c34d7-108">Input data in `HTerm[]` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="c34d7-109">termType: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c34d7-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c34d7-110">추가 정보를 GeneratorIndex에 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c34d7-110">Additional information added to GeneratorIndex.</span></span>


### <a name="idx--int"></a><span data-ttu-id="c34d7-111">idx: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c34d7-111">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c34d7-112">Hamiltonian의 용어에 대 한 인덱스</span><span class="sxs-lookup"><span data-stu-id="c34d7-112">Index to a term of the Hamiltonian</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="c34d7-113">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c34d7-113">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="c34d7-114">가 나타내는 Hamiltonian 용어를에 `data[idx]` 의해 추가 된 추가 정보와 함께 나타내는 GeneratorIndex `termType` 입니다.</span><span class="sxs-lookup"><span data-stu-id="c34d7-114">A GeneratorIndex representing a Hamiltonian term represented by `data[idx]`, together with additional information added by `termType`.</span></span>