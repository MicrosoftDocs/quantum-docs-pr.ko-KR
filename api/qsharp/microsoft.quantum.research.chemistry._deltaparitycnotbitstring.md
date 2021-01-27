---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 3dd2d299a094577d377780d731e76287815e8d03
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847596"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="d179b-102">_DeltaParityCNOTbitstring 함수</span><span class="sxs-lookup"><span data-stu-id="d179b-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="d179b-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="d179b-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="d179b-104">패키지: [Microsoft](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="d179b-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="d179b-105">의 클래식 처리 단계입니다 `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="d179b-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="d179b-106">이는 두 PQRS 사이의 패리티 차이를 평가 하기 위한 제어 비트 목록을 계산 합니다. 짝수의 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="d179b-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="d179b-107">입력</span><span class="sxs-lookup"><span data-stu-id="d179b-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="d179b-108">prevFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d179b-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="d179b-109">nextFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d179b-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="d179b-110">Output: ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="d179b-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="d179b-111">설명</span><span class="sxs-lookup"><span data-stu-id="d179b-111">Remarks</span></span>

<span data-ttu-id="d179b-112">여기서는 용어 길이가 짝수 라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d179b-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="d179b-113">두 용어 사이의 패리티 차이에 대 한 컨트롤 목록을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d179b-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="d179b-114">여기서는 입력 목록이 오름차순으로 정렬 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d179b-114">This assumes that the input lists is sorted in ascending order.</span></span>