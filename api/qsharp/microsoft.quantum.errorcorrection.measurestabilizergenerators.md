---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: MeasureStabilizerGenerators 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: 6c048c17df21d1026dc671f30d72a13ed8d8b7f5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200631"
---
# <a name="measurestabilizergenerators-operation"></a><span data-ttu-id="0e66d-102">MeasureStabilizerGenerators 작업</span><span class="sxs-lookup"><span data-stu-id="0e66d-102">MeasureStabilizerGenerators operation</span></span>

<span data-ttu-id="0e66d-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="0e66d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="0e66d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0e66d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0e66d-105">안정기 그룹의 지정 된 생성기 집합을 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-105">Measures the given set of generators of a stabilizer group.</span></span>

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a><span data-ttu-id="0e66d-106">입력</span><span class="sxs-lookup"><span data-stu-id="0e66d-106">Input</span></span>

### <a name="stabilizergroup--pauli"></a><span data-ttu-id="0e66d-107">stabilizerGroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="0e66d-107">stabilizerGroup : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="0e66d-108">Multiqubit Pauli 연산자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-108">An array of multiqubit Pauli operators.</span></span>
<span data-ttu-id="0e66d-109">예를 들어 `stabilizerGroup[0]` 는 안정기 생성기 인 텐서 곱 인 단일 수준 비트 Pauli 행렬의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-109">For example, `stabilizerGroup[0]` is a list of single-qubit Pauli matrices, the tensor product of which is a stabilizer generator.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="0e66d-110">logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="0e66d-110">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="0e66d-111">안정기 코드가 정의 된 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-111">An array of qubits where the stabilizer code is defined.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="0e66d-112">가젯: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => __잘못 되었습니다 <Result>__ .</span><span class="sxs-lookup"><span data-stu-id="0e66d-112">gadget : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="0e66d-113">Multiqubit Pauli 연산자를 측정 하는 방법을 지정 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-113">An operation that specifies how to measure a multiqubit Pauli operator.</span></span>



## <a name="output--syndrome"></a><span data-ttu-id="0e66d-114">출력: [증후군](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="0e66d-114">Output : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="0e66d-115">측정값의 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-115">The result of measurements.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e66d-116">설명</span><span class="sxs-lookup"><span data-stu-id="0e66d-116">Remarks</span></span>

<span data-ttu-id="0e66d-117">이는 지정 된 생성기 집합이 통근 이나 출장 여부를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-117">This does not check if the given set of generators are commuting.</span></span>
<span data-ttu-id="0e66d-118">통근 이나 출장 않는 경우에는 측정값의 결과가 임의로 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e66d-118">If they are not commuting, the result of measurements may be arbitrary.</span></span>