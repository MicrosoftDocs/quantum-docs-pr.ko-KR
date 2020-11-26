---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: ApplyTransposition 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: ca22b090f2b2613f07caef698941ea608374ab1e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203317"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="eacc7-102">ApplyTransposition 작업</span><span class="sxs-lookup"><span data-stu-id="eacc7-102">ApplyTransposition operation</span></span>

<span data-ttu-id="eacc7-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="eacc7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="eacc7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eacc7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="eacc7-105">Description</span><span class="sxs-lookup"><span data-stu-id="eacc7-105">Description</span></span>

<span data-ttu-id="eacc7-106">이 작업을 수행 하면 `a` `b` 길이가 $n $ 인 지정 된 상태 vector의 인덱스에 있는 진폭을 인덱스에 있는 진폭으로 바꿉니다 `register` .</span><span class="sxs-lookup"><span data-stu-id="eacc7-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="eacc7-107">`a`가와 같으면 `b` 상태 벡터는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eacc7-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="eacc7-108">입력</span><span class="sxs-lookup"><span data-stu-id="eacc7-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="eacc7-109">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eacc7-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eacc7-110">첫 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)</span><span class="sxs-lookup"><span data-stu-id="eacc7-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="eacc7-111">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eacc7-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eacc7-112">두 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)</span><span class="sxs-lookup"><span data-stu-id="eacc7-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="eacc7-113">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="eacc7-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="eacc7-114">Transposition이 적용 되는 $ $n의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="eacc7-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eacc7-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eacc7-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

