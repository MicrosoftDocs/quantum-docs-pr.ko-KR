---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerOptimizedBlockEncodingStatePrep
title: _JordanWignerOptimizedBlockEncodingStatePrep 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerOptimizedBlockEncodingStatePrep
qsharp.summary: ''
ms.openlocfilehash: 492248b49faf594adcd37550db9172a17bf02fad
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851577"
---
# <a name="_jordanwigneroptimizedblockencodingstateprep-operation"></a><span data-ttu-id="cfc7b-102">_JordanWignerOptimizedBlockEncodingStatePrep 작업</span><span class="sxs-lookup"><span data-stu-id="cfc7b-102">_JordanWignerOptimizedBlockEncodingStatePrep operation</span></span>

<span data-ttu-id="cfc7b-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="cfc7b-104">패키지: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>




```qsharp
operation _JordanWignerOptimizedBlockEncodingStatePrep (targetError : Double, optimizedBEGeneratorSystem : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem, qROMIdxRegister : Microsoft.Quantum.Arithmetic.LittleEndian, qROMGarbage : Qubit[], signQubit : Qubit, selectZControlRegisters : Qubit[], OptimizedBEControlRegisters : Qubit[], pauliBases : Qubit[], pauliBasesIdx : Microsoft.Quantum.Arithmetic.LittleEndian, indexRegisters : Microsoft.Quantum.Arithmetic.LittleEndian[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cfc7b-105">입력</span><span class="sxs-lookup"><span data-stu-id="cfc7b-105">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="cfc7b-106">targetError: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-106">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="optimizedbegeneratorsystem--optimizedbegeneratorsystem"></a><span data-ttu-id="cfc7b-107">optimizedBEGeneratorSystem: [optimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-107">optimizedBEGeneratorSystem : [OptimizedBEGeneratorSystem](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem)</span></span>




### <a name="qromidxregister--littleendian"></a><span data-ttu-id="cfc7b-108">qROMIdxRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-108">qROMIdxRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="qromgarbage--qubit"></a><span data-ttu-id="cfc7b-109">qROMGarbage: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cfc7b-109">qROMGarbage : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="signqubit--qubit"></a><span data-ttu-id="cfc7b-110">Sign의 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-110">signQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="selectzcontrolregisters--qubit"></a><span data-ttu-id="cfc7b-111">selectZControlRegisters: [해당](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cfc7b-111">selectZControlRegisters : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="optimizedbecontrolregisters--qubit"></a><span data-ttu-id="cfc7b-112">OptimizedBEControlRegisters: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cfc7b-112">OptimizedBEControlRegisters : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="paulibases--qubit"></a><span data-ttu-id="cfc7b-113">pauliBases: [](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cfc7b-113">pauliBases : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="paulibasesidx--littleendian"></a><span data-ttu-id="cfc7b-114">pauliBasesIdx: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-114">pauliBasesIdx : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="indexregisters--littleendian"></a><span data-ttu-id="cfc7b-115">indexRegisters: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]</span><span class="sxs-lookup"><span data-stu-id="cfc7b-115">indexRegisters : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="cfc7b-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cfc7b-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

