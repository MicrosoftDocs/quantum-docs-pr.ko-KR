---
uid: Microsoft.Quantum.Chemistry.HTermToGenIdx
title: HTermToGenIdx 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: HTermToGenIdx
qsharp.summary: Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.
ms.openlocfilehash: dd72355adb32f9a0d109ee36b24be2d445f3fa66
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714834"
---
# <a name="htermtogenidx-function"></a><span data-ttu-id="eae4b-102">HTermToGenIdx 함수</span><span class="sxs-lookup"><span data-stu-id="eae4b-102">HTermToGenIdx function</span></span>

<span data-ttu-id="eae4b-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="eae4b-103">Namespace: [Microsoft.Quantum.Chemistry](xref:Microsoft.Quantum.Chemistry)</span></span>

<span data-ttu-id="eae4b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eae4b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eae4b-105">데이터 형식의 Hamiltonian 항을 `HTerm` GeneratorIndex로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae4b-105">Converts a Hamiltonian term in `HTerm` data format to a GeneratorIndex.</span></span>

```qsharp
function HTermToGenIdx (term : Microsoft.Quantum.Chemistry.HTerm, termType : Int[]) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="eae4b-106">입력</span><span class="sxs-lookup"><span data-stu-id="eae4b-106">Input</span></span>

### <a name="term--hterm"></a><span data-ttu-id="eae4b-107">용어: [Hterm](xref:Microsoft.Quantum.Chemistry.HTerm)</span><span class="sxs-lookup"><span data-stu-id="eae4b-107">term : [HTerm](xref:Microsoft.Quantum.Chemistry.HTerm)</span></span>

<span data-ttu-id="eae4b-108">형식의 입력 데이터 `HTerm` 입니다.</span><span class="sxs-lookup"><span data-stu-id="eae4b-108">Input data in `HTerm` format.</span></span>


### <a name="termtype--int"></a><span data-ttu-id="eae4b-109">termType: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="eae4b-109">termType : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="eae4b-110">추가 정보를 GeneratorIndex에 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="eae4b-110">Additional information added to GeneratorIndex.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="eae4b-111">출력: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="eae4b-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="eae4b-112">가 나타내는 Hamiltonian 용어를에 `term` 의해 추가 된 추가 정보와 함께 나타내는 GeneratorIndex `termType` 입니다.</span><span class="sxs-lookup"><span data-stu-id="eae4b-112">A GeneratorIndex representing a Hamiltonian term represented by `term`, together with additional information added by `termType`.</span></span>