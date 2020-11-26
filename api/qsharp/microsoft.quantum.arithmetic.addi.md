---
uid: Microsoft.Quantum.Arithmetic.AddI
title: AddI 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: 9a90d15defd57cf2836a6fda5b52ddaa816fd55e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191026"
---
# <a name="addi-operation"></a><span data-ttu-id="19547-102">AddI 작업</span><span class="sxs-lookup"><span data-stu-id="19547-102">AddI operation</span></span>

<span data-ttu-id="19547-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="19547-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="19547-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="19547-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="19547-105">는의 레지스터 크기에 따라의 추가 및 포함 없이 추가를 자동으로 선택 `ys` 합니다.</span><span class="sxs-lookup"><span data-stu-id="19547-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="19547-106">입력</span><span class="sxs-lookup"><span data-stu-id="19547-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="19547-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19547-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="19547-108">$ 비트 addend를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="19547-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="19547-109">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="19547-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="19547-110">최소 $n $ 이상 비트를 사용 하 여 addend를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19547-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="19547-111">는 결과를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="19547-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="19547-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19547-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

