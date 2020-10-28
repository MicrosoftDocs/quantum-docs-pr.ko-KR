---
uid: Microsoft.Quantum.MachineLearning.StateGenerator
title: StateGenerator 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: StateGenerator
qsharp.summary: Describes an operation that prepares a given input to a sequential classifier.
ms.openlocfilehash: e3026dbae7209acd41924c0038a6f9b2c4b41197
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722398"
---
# <a name="stategenerator-user-defined-type"></a><span data-ttu-id="2f4aa-102">StateGenerator 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="2f4aa-102">StateGenerator user defined type</span></span>

<span data-ttu-id="2f4aa-103">네임 스페이스: [MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2f4aa-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2f4aa-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2f4aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2f4aa-105">순차적 분류자에 대해 지정 된 입력을 준비 하는 작업을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-105">Describes an operation that prepares a given input to a sequential classifier.</span></span>

```qsharp

newtype StateGenerator = (NQubits : Int, Prepare : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="2f4aa-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="2f4aa-106">Named Items</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="2f4aa-107">N Bits: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2f4aa-107">NQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2f4aa-108">인코딩된 입력이 정의 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2f4aa-108">The number of qubits on which the encoded input is defined.</span></span>
### <a name="prepare--littleendian--unit-adj--ctl"></a><span data-ttu-id="2f4aa-109">준비: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="2f4aa-109">Prepare : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="2f4aa-110">비트의 작은 endian 레지스터에서 인코딩된 입력을 준비 하는 연산입니다 `NQubits` .</span><span class="sxs-lookup"><span data-stu-id="2f4aa-110">An operation which prepares the encoded input on a little-endian register of `NQubits` qubits.</span></span>