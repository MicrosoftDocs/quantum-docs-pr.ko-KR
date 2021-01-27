---
uid: Microsoft.Quantum.Preparation._CompileApproximateArbitraryStatePreparation
title: _CompileApproximateArbitraryStatePreparation 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: _CompileApproximateArbitraryStatePreparation
qsharp.summary: ''
ms.openlocfilehash: 523e369cc109fb06afe0fdaae5efdf376d7934d7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842479"
---
# <a name="_compileapproximatearbitrarystatepreparation-function"></a><span data-ttu-id="cb48f-102">_CompileApproximateArbitraryStatePreparation 함수</span><span class="sxs-lookup"><span data-stu-id="cb48f-102">_CompileApproximateArbitraryStatePreparation function</span></span>

<span data-ttu-id="cb48f-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="cb48f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="cb48f-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cb48f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
function _CompileApproximateArbitraryStatePreparation (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], nQubits : Int) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="cb48f-105">입력</span><span class="sxs-lookup"><span data-stu-id="cb48f-105">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="cb48f-106">허용 오차: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cb48f-106">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="coefficients--complexpolar"></a><span data-ttu-id="cb48f-107">계수: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="cb48f-107">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>




### <a name="nqubits--int"></a><span data-ttu-id="cb48f-108">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cb48f-108">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="cb48f-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="cb48f-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

