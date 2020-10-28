---
uid: Microsoft.Quantum.Characterization.ApplyHadamardTest
title: ApplyHadamardTest 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ApplyHadamardTest
qsharp.summary: ''
ms.openlocfilehash: 6fcbc81faa7c177874d102041daacd4e62a97737
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715128"
---
# <a name="applyhadamardtest-operation"></a><span data-ttu-id="5b870-102">ApplyHadamardTest 작업</span><span class="sxs-lookup"><span data-stu-id="5b870-102">ApplyHadamardTest operation</span></span>

<span data-ttu-id="5b870-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="5b870-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="5b870-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b870-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyHadamardTest (phaseShift : Bool, commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), control : Qubit, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5b870-105">입력</span><span class="sxs-lookup"><span data-stu-id="5b870-105">Input</span></span>

### <a name="phaseshift--bool"></a><span data-ttu-id="5b870-106">phaseShift: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5b870-106">phaseShift : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="commonpreparation--qubit--unit-adj"></a><span data-ttu-id="5b870-107">commonPreparation: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b870-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="preparation1--qubit--unit-adj--ctl"></a><span data-ttu-id="5b870-108">preparation1: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="5b870-108">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="preparation2--qubit--unit-adj--ctl"></a><span data-ttu-id="5b870-109">preparation2: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="5b870-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="control--qubit"></a><span data-ttu-id="5b870-110">제어: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b870-110">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="target--qubit"></a><span data-ttu-id="5b870-111">target: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b870-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="5b870-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b870-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

