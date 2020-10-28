---
uid: Microsoft.Quantum.Arithmetic.AddI
title: AddI 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 7ee2b9099ea65b95647422dadc1efe4bf043d147
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721688"
---
# <a name="addi-operation"></a><span data-ttu-id="06206-102">AddI 작업</span><span class="sxs-lookup"><span data-stu-id="06206-102">AddI operation</span></span>

<span data-ttu-id="06206-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="06206-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="06206-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="06206-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="06206-105">는의 레지스터 크기에 따라의 추가 및 포함 없이 추가를 자동으로 선택 `ys` 합니다.</span><span class="sxs-lookup"><span data-stu-id="06206-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="06206-106">입력</span><span class="sxs-lookup"><span data-stu-id="06206-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="06206-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="06206-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="06206-108">$ 비트 addend를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="06206-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="06206-109">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="06206-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="06206-110">최소 $n $ 이상 비트를 사용 하 여 addend를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06206-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="06206-111">는 결과를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="06206-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="06206-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="06206-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

