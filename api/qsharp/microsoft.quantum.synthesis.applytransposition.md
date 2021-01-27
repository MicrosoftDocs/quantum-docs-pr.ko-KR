---
uid: Microsoft.Quantum.Synthesis.ApplyTransposition
title: ApplyTransposition 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyTransposition
qsharp.summary: ''
ms.openlocfilehash: 46cf8c2c891aa02b0d8a1397e6c2b7a4b8618048
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855574"
---
# <a name="applytransposition-operation"></a><span data-ttu-id="6bc7a-102">ApplyTransposition 작업</span><span class="sxs-lookup"><span data-stu-id="6bc7a-102">ApplyTransposition operation</span></span>

<span data-ttu-id="6bc7a-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6bc7a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>




```qsharp
operation ApplyTransposition (a : Int, b : Int, qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="6bc7a-105">설명</span><span class="sxs-lookup"><span data-stu-id="6bc7a-105">Description</span></span>

<span data-ttu-id="6bc7a-106">이 작업을 수행 하면 `a` `b` 길이가 $n $ 인 지정 된 상태 vector의 인덱스에 있는 진폭을 인덱스에 있는 진폭으로 바꿉니다 `register` .</span><span class="sxs-lookup"><span data-stu-id="6bc7a-106">This operation swaps the amplitude at index `a` with the amplitude at index `b` in the given state-vector of `register` of length $n$.</span></span>  <span data-ttu-id="6bc7a-107">`a`가와 같으면 `b` 상태 벡터는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-107">If `a` equals `b`, the state-vector is not changed.</span></span>

## <a name="input"></a><span data-ttu-id="6bc7a-108">입력</span><span class="sxs-lookup"><span data-stu-id="6bc7a-108">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="6bc7a-109">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-109">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6bc7a-110">첫 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-110">First index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="b--int"></a><span data-ttu-id="6bc7a-111">b: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-111">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6bc7a-112">두 번째 인덱스 (0에서 $2 ^ n-$1 사이의 값 이어야 함)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-112">Second index (must be a value from 0 to $2^n - 1$)</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="6bc7a-113">작업 비트: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6bc7a-114">Transposition이 적용 되는 $ $n의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-114">A list of $n$ qubits to which the transposition is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6bc7a-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6bc7a-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="6bc7a-116">예</span><span class="sxs-lookup"><span data-stu-id="6bc7a-116">Example</span></span>

<span data-ttu-id="6bc7a-117">Superposition의 숫자 상태 $ | 1 \ rangle $, $ | 2 \ rangle $ 및 $ | 3 \ rangle $ on 2를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bc7a-117">Prepare a uniform superposition of number states $|1\rangle$, $|2\rangle$, and $|3\rangle$ on 2 qubits.</span></span>

```qsharp
using (qubits = Qubit[2]) {
  let register = LittleEndian(qubits);
  PrepareUniformSuperposition(3, register);
  ApplyTransposition(0, 3, register);
}
```