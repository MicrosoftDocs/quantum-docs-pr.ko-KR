---
uid: Microsoft.Quantum.Preparation.PrepareQuantumROMState
title: PrepareQuantumROMState 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQuantumROMState
qsharp.summary: ''
ms.openlocfilehash: 41b3a041ad3cef466e780fa9e88ab8ab72269e66
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193508"
---
# <a name="preparequantumromstate-operation"></a><span data-ttu-id="fb656-102">PrepareQuantumROMState 작업</span><span class="sxs-lookup"><span data-stu-id="fb656-102">PrepareQuantumROMState operation</span></span>

<span data-ttu-id="fb656-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="fb656-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="fb656-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fb656-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation PrepareQuantumROMState (nBitsPrecision : Int, nCoeffs : Int, nBitsIndices : Int, keepCoeff : Int[], altIndex : Int[], data : Bool[][], indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, dataQubits : Qubit[], garbageRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fb656-105">입력</span><span class="sxs-lookup"><span data-stu-id="fb656-105">Input</span></span>

### <a name="nbitsprecision--int"></a><span data-ttu-id="fb656-106">nBitsPrecision: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fb656-106">nBitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ncoeffs--int"></a><span data-ttu-id="fb656-107">nCoeffs: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fb656-107">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="nbitsindices--int"></a><span data-ttu-id="fb656-108">nBitsIndices: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fb656-108">nBitsIndices : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="keepcoeff--int"></a><span data-ttu-id="fb656-109">keepCoeff: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fb656-109">keepCoeff : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="altindex--int"></a><span data-ttu-id="fb656-110">altIndex: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="fb656-110">altIndex : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="data--bool"></a><span data-ttu-id="fb656-111">데이터: [Bool](xref:microsoft.quantum.lang-ref.bool)[] []</span><span class="sxs-lookup"><span data-stu-id="fb656-111">data : [Bool](xref:microsoft.quantum.lang-ref.bool)[][]</span></span>




### <a name="indexregister--littleendian"></a><span data-ttu-id="fb656-112">indexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fb656-112">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="dataqubits--qubit"></a><span data-ttu-id="fb656-113">dataQubits: [\Bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fb656-113">dataQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="garbageregister--qubit"></a><span data-ttu-id="fb656-114">garbageRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fb656-114">garbageRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="fb656-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fb656-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

