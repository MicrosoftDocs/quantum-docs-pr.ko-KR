---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: StateGenerator 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: b4f6c3ca28e2976b6a0d58f4ef25ea943de9811e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854884"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="b09bb-102">StateGenerator 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="b09bb-102">StateGenerator user defined type</span></span>

<span data-ttu-id="b09bb-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b09bb-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b09bb-104">패키지: [MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b09bb-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="b09bb-105">순차적 분류자에 대해 지정 된 입력을 준비 하는 작업을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b09bb-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="b09bb-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="b09bb-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="b09bb-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b09bb-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b09bb-108">인코딩된 입력이 정의 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b09bb-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="b09bb-109">준비: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="b09bb-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="b09bb-110">비트의 작은 endian 레지스터에서 인코딩된 입력을 준비 하는 연산입니다 `NQubits` .</span><span class="sxs-lookup"><span data-stu-id="b09bb-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>