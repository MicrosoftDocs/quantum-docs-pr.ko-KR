---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: BlochSphereCoordinates 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 594896a72fe40e5ba994e08500c3ce71b185bfff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193559"
---
# <a name="blochspherecoordinates-function"></a><span data-ttu-id="153f4-102">BlochSphereCoordinates 함수</span><span class="sxs-lookup"><span data-stu-id="153f4-102">BlochSphereCoordinates function</span></span>

<span data-ttu-id="153f4-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="153f4-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="153f4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="153f4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="153f4-105">단일가 나 비트 상태에 대 한 Bloch 구 좌표를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="153f4-105">Computes the Bloch sphere coordinates for a single-qubit state.</span></span>

<span data-ttu-id="153f4-106">지정 된 두 복소수 $a 0, a1 $는 Bloch 구의 좌표를 계산 하는 구의 좌표를 계산 하는 구의 좌표를 계산 합니다. 예를 들어, $a 0 \ket {0} + a1 \ket {1} = r e ^ {it} (e ^ {-i \emlb = r e ^ {(\ 테타/2)} \ket {0} + e ^ {i \emlc\sin{(\ 테타 {1}</span><span class="sxs-lookup"><span data-stu-id="153f4-106">Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.</span></span>

```qsharp
function BlochSphereCoordinates (a0 : Microsoft.Quantum.Math.ComplexPolar, a1 : Microsoft.Quantum.Math.ComplexPolar) : (Microsoft.Quantum.Math.ComplexPolar, Double, Double)
```


## <a name="input"></a><span data-ttu-id="153f4-107">입력</span><span class="sxs-lookup"><span data-stu-id="153f4-107">Input</span></span>

### <a name="a0--complexpolar"></a><span data-ttu-id="153f4-108">a0: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="153f4-108">a0 : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="153f4-109">상태 $ \ket $의 복합 계수입니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="153f4-109">Complex coefficient of state $\ket{0}$.</span></span>


### <a name="a1--complexpolar"></a><span data-ttu-id="153f4-110">a1: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="153f4-110">a1 : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="153f4-111">상태 $ \ket $의 복합 계수입니다 {1} .</span><span class="sxs-lookup"><span data-stu-id="153f4-111">Complex coefficient of state $\ket{1}$.</span></span>



## <a name="output--complexpolardoubledouble"></a><span data-ttu-id="153f4-112">출력: ([Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar),[double](xref:microsoft.quantum.lang-ref.double),[double](xref:microsoft.quantum.lang-ref.double))</span><span class="sxs-lookup"><span data-stu-id="153f4-112">Output : ([ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar),[Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))</span></span>

<span data-ttu-id="153f4-113">을 포함 하는 튜플입니다 `(ComplexPolar(r, t), phi, theta)` .</span><span class="sxs-lookup"><span data-stu-id="153f4-113">A tuple containing `(ComplexPolar(r, t), phi, theta)`.</span></span>