---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: StateGenerator 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: 5c9643f5c917ff3cb25fa8c046856b03cc287edd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211562"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="37b7c-102">StateGenerator 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="37b7c-102">StateGenerator user defined type</span></span>

<span data-ttu-id="37b7c-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="37b7c-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="37b7c-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="37b7c-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="37b7c-105">순차적 분류자에 대해 지정 된 입력을 준비 하는 작업을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b7c-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="37b7c-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="37b7c-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="37b7c-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="37b7c-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="37b7c-108">인코딩된 입력이 정의 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="37b7c-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="37b7c-109">준비: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="37b7c-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="37b7c-110">비트의 작은 endian 레지스터에서 인코딩된 입력을 준비 하는 연산입니다 `NQubits` .</span><span class="sxs-lookup"><span data-stu-id="37b7c-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>