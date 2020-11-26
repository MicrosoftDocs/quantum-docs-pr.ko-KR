---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: QuantumROMQubitCount 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: >-
  > [!WARNING]

  > QuantumROMQubitCount has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.


  Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 0ec1e042b9f675505f73bfcdcc6706d0bc0367df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210406"
---
# <a name="quantumromqubitcount-function"></a><span data-ttu-id="cc612-102">QuantumROMQubitCount 함수</span><span class="sxs-lookup"><span data-stu-id="cc612-102">QuantumROMQubitCount function</span></span>

<span data-ttu-id="cc612-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="cc612-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="cc612-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc612-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="cc612-105">QuantumROMQubitCount는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc612-105">QuantumROMQubitCount has been deprecated.</span></span> <span data-ttu-id="cc612-106">대신 <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements>를 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="cc612-106">Please use <xref:Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements> instead.</span></span>

<span data-ttu-id="cc612-107">에서 반환 하는 작업에 할당 해야 하는 총 작업 수를 반환 합니다 `QuantumROM` .</span><span class="sxs-lookup"><span data-stu-id="cc612-107">Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.</span></span>

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a><span data-ttu-id="cc612-108">입력</span><span class="sxs-lookup"><span data-stu-id="cc612-108">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="cc612-109">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cc612-109">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cc612-110">$ \Epsilon $ 대상 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="cc612-110">The target error $\epsilon$.</span></span>


### <a name="ncoeffs--int"></a><span data-ttu-id="cc612-111">nCoeffs: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cc612-111">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cc612-112">에 지정 된 계수 수 `QuantumROM` 입니다.</span><span class="sxs-lookup"><span data-stu-id="cc612-112">Number of coefficients specified in `QuantumROM`.</span></span>



## <a name="output--intintint"></a><span data-ttu-id="cc612-113">Output[: (int,](xref:microsoft.quantum.lang-ref.int)([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))</span><span class="sxs-lookup"><span data-stu-id="cc612-113">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int)))</span></span>

## <a name="first-parameter"></a><span data-ttu-id="cc612-114">첫 번째 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cc612-114">First parameter</span></span>

<span data-ttu-id="cc612-115">`(x,(y,z))`는 할당 된 총 수 인 튜플을,는 레지스터의 값이 고,은 `x = y + z` `y` 가비지 비트 수입니다 `LittleEndian` `z` .</span><span class="sxs-lookup"><span data-stu-id="cc612-115">A tuple `(x,(y,z))` where `x = y + z` is the total number of qubits allocated, `y` is the number of qubits for the `LittleEndian` register, and `z` is the Number of garbage qubits.</span></span>