---
uid: Microsoft.Quantum.Arithmetic.AddI
title: AddI 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddI
qsharp.summary: Automatically chooses between addition with carry and without, depending on the register size of `ys`.
ms.openlocfilehash: a17403652cc2b2712defe52112a3ac599330da9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843842"
---
# <a name="addi-operation"></a><span data-ttu-id="17e73-102">AddI 작업</span><span class="sxs-lookup"><span data-stu-id="17e73-102">AddI operation</span></span>

<span data-ttu-id="17e73-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="17e73-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="17e73-104">Package: [Microsoft 양자](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="17e73-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="17e73-105">는의 레지스터 크기에 따라의 추가 및 포함 없이 추가를 자동으로 선택 `ys` 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e73-105">Automatically chooses between addition with carry and without, depending on the register size of `ys`.</span></span>

```qsharp
operation AddI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="17e73-106">입력</span><span class="sxs-lookup"><span data-stu-id="17e73-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="17e73-107">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="17e73-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="17e73-108">$ 비트 addend를 $n 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e73-108">$n$-bit addend.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="17e73-109">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="17e73-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="17e73-110">최소 $n $ 이상 비트를 사용 하 여 addend를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e73-110">Addend with at least $n$ qubits.</span></span> <span data-ttu-id="17e73-111">는 결과를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e73-111">Will hold the result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="17e73-112">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="17e73-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

