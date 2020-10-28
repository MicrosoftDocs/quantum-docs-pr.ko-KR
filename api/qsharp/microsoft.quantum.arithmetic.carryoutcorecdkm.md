---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: CarryOutCoreCDKM 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 6a292e66f6d9911d2a9075f6397f4f5ba97ec64d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721304"
---
# <a name="carryoutcorecdkm-operation"></a><span data-ttu-id="05701-102">CarryOutCoreCDKM 작업</span><span class="sxs-lookup"><span data-stu-id="05701-102">CarryOutCoreCDKM operation</span></span>

<span data-ttu-id="05701-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="05701-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="05701-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="05701-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="05701-105">위의 ApplyOuterCDKMAdder 작업과 함께 사용 되는 RippleCarryAdderCDKM의 핵심 작업입니다. 즉, RippleCarryAdderCDKM의 내부 작업을 가져오기 위해이 작업을 conjugated 합니다.</span><span class="sxs-lookup"><span data-stu-id="05701-105">The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM.</span></span> <span data-ttu-id="05701-106">이 작업을 수행 하면 작업을 계산 하 여 입력의 일부에 대 한 게이트 없는 시퀀스를 적용 합니다 `ys` .</span><span class="sxs-lookup"><span data-stu-id="05701-106">This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.</span></span>

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="05701-107">입력</span><span class="sxs-lookup"><span data-stu-id="05701-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="05701-108">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="05701-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="05701-109">첫 번째 비트율 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="05701-109">First qubit register.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="05701-110">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="05701-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="05701-111">두 번째 비트율 비트 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="05701-111">Second qubit register.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="05701-112">ancilla: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="05701-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="05701-113">이 작업에 전달 된 RippleCarryAdderCDKM에서 사용 되는 ancilla 이상 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="05701-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="05701-114">운반: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="05701-114">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="05701-115">RippleCarryAdderCDKM 작업에서 이상 비트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="05701-115">Carry out qubit in the RippleCarryAdderCDKM operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="05701-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="05701-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="05701-117">참조</span><span class="sxs-lookup"><span data-stu-id="05701-117">References</span></span>

- <span data-ttu-id="05701-118">Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new 퀀텀 ripple and A new, 2004.</span><span class="sxs-lookup"><span data-stu-id="05701-118">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1