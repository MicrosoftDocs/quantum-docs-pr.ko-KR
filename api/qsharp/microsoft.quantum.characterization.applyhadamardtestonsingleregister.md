---
uid: Microsoft.Quantum.Characterization.ApplyHadamardTestOnSingleRegister
title: ApplyHadamardTestOnSingleRegister 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ApplyHadamardTestOnSingleRegister
qsharp.summary: ''
ms.openlocfilehash: e67fa076f76c798a0252a589d045da79d09ea256
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715114"
---
# <a name="applyhadamardtestonsingleregister-operation"></a><span data-ttu-id="994a0-102">ApplyHadamardTestOnSingleRegister 작업</span><span class="sxs-lookup"><span data-stu-id="994a0-102">ApplyHadamardTestOnSingleRegister operation</span></span>

<span data-ttu-id="994a0-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="994a0-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="994a0-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="994a0-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyHadamardTestOnSingleRegister (phaseShift : Bool, commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="994a0-105">입력</span><span class="sxs-lookup"><span data-stu-id="994a0-105">Input</span></span>

### <a name="phaseshift--bool"></a><span data-ttu-id="994a0-106">phaseShift: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="994a0-106">phaseShift : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="commonpreparation--qubit--unit-adj"></a><span data-ttu-id="994a0-107">commonPreparation: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="994a0-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>




### <a name="preparation1--qubit--unit-adj--ctl"></a><span data-ttu-id="994a0-108">preparation1: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="994a0-108">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="preparation2--qubit--unit-adj--ctl"></a><span data-ttu-id="994a0-109">preparation2: [Adj](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="994a0-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="register--qubit"></a><span data-ttu-id="994a0-110">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="994a0-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--unit"></a><span data-ttu-id="994a0-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="994a0-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

