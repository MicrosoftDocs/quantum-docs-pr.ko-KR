---
uid: Microsoft.Quantum.Preparation.WriteQuantumROMBitString
title: Writ의 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: WriteQuantumROMBitString
qsharp.summary: ''
ms.openlocfilehash: cee30a37cca418b6d0122416ce122576511cf303
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193185"
---
# <a name="writequantumrombitstring-operation"></a><span data-ttu-id="54db3-102">Writ의 작업</span><span class="sxs-lookup"><span data-stu-id="54db3-102">WriteQuantumROMBitString operation</span></span>

<span data-ttu-id="54db3-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="54db3-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="54db3-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="54db3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation WriteQuantumROMBitString (idx : Int, keepCoeff : Int[], altIndex : Int[], data : Bool[][], keepCoeffRegister : Microsoft.Quantum.Arithmetic.LittleEndian, altIndexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, dataRegister : Qubit[], altDataRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="54db3-105">입력</span><span class="sxs-lookup"><span data-stu-id="54db3-105">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="54db3-106">idx: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="54db3-106">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="keepcoeff--int"></a><span data-ttu-id="54db3-107">keepCoeff: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="54db3-107">keepCoeff : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="altindex--int"></a><span data-ttu-id="54db3-108">altIndex: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="54db3-108">altIndex : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="data--bool"></a><span data-ttu-id="54db3-109">데이터: [Bool](xref:microsoft.quantum.lang-ref.bool)[] []</span><span class="sxs-lookup"><span data-stu-id="54db3-109">data : [Bool](xref:microsoft.quantum.lang-ref.bool)[][]</span></span>




### <a name="keepcoeffregister--littleendian"></a><span data-ttu-id="54db3-110">keepCoeffRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="54db3-110">keepCoeffRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="altindexregister--littleendian"></a><span data-ttu-id="54db3-111">altIndexRegister: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="54db3-111">altIndexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="dataregister--qubit"></a><span data-ttu-id="54db3-112">dataRegister: [\Bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="54db3-112">dataRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="altdataregister--qubit"></a><span data-ttu-id="54db3-113">altDataRegister: [\Bit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="54db3-113">altDataRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="54db3-114">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="54db3-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

