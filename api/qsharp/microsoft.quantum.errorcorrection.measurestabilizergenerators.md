---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: MeasureStabilizerGenerators 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: a3f48ff24a39d13a57f7a144e21d4e41bb8a8b49
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712265"
---
# <a name="measurestabilizergenerators-operation"></a><span data-ttu-id="f2a92-102">MeasureStabilizerGenerators 작업</span><span class="sxs-lookup"><span data-stu-id="f2a92-102">MeasureStabilizerGenerators operation</span></span>

<span data-ttu-id="f2a92-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="f2a92-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="f2a92-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f2a92-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f2a92-105">안정기 그룹의 지정 된 생성기 집합을 측정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-105">Measures the given set of generators of a stabilizer group.</span></span>

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a><span data-ttu-id="f2a92-106">입력</span><span class="sxs-lookup"><span data-stu-id="f2a92-106">Input</span></span>

### <a name="stabilizergroup--pauli"></a><span data-ttu-id="f2a92-107">stabilizerGroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="f2a92-107">stabilizerGroup : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="f2a92-108">Multiqubit Pauli 연산자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-108">An array of multiqubit Pauli operators.</span></span>
<span data-ttu-id="f2a92-109">예를 들어 `stabilizerGroup[0]` 는 안정기 생성기 인 텐서 곱 인 단일 수준 비트 Pauli 행렬의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-109">For example, `stabilizerGroup[0]` is a list of single-qubit Pauli matrices, the tensor product of which is a stabilizer generator.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="f2a92-110">logicalRegister: [Logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="f2a92-110">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="f2a92-111">안정기 코드가 정의 된 요소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-111">An array of qubits where the stabilizer code is defined.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="f2a92-112">가젯: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[[], [](xref:microsoft.quantum.lang-ref.qubit)]) => __잘못 되었습니다 <Result>__ .</span><span class="sxs-lookup"><span data-stu-id="f2a92-112">gadget : ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="f2a92-113">Multiqubit Pauli 연산자를 측정 하는 방법을 지정 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-113">An operation that specifies how to measure a multiqubit Pauli operator.</span></span>



## <a name="output--syndrome"></a><span data-ttu-id="f2a92-114">출력: [증후군](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="f2a92-114">Output : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="f2a92-115">측정값의 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-115">The result of measurements.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2a92-116">설명</span><span class="sxs-lookup"><span data-stu-id="f2a92-116">Remarks</span></span>

<span data-ttu-id="f2a92-117">이는 지정 된 생성기 집합이 통근 이나 출장 여부를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-117">This does not check if the given set of generators are commuting.</span></span>
<span data-ttu-id="f2a92-118">통근 이나 출장 않는 경우에는 측정값의 결과가 임의로 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2a92-118">If they are not commuting, the result of measurements may be arbitrary.</span></span>