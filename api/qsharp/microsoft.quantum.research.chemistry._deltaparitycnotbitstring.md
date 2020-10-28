---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: _DeltaParityCNOTbitstring 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 95b4c2df05f32cb937ec2cf421f43f2fdbf319da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710851"
---
# <a name="_deltaparitycnotbitstring-function"></a><span data-ttu-id="1d94e-102">_DeltaParityCNOTbitstring 함수</span><span class="sxs-lookup"><span data-stu-id="1d94e-102">_DeltaParityCNOTbitstring function</span></span>

<span data-ttu-id="1d94e-103">네임 스페이스: [Microsoft](xref:Microsoft.Quantum.Research.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="1d94e-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="1d94e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1d94e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1d94e-105">의 클래식 처리 단계입니다 `ApplyDeltaParity` .</span><span class="sxs-lookup"><span data-stu-id="1d94e-105">Classical processing step of `ApplyDeltaParity`.</span></span>
<span data-ttu-id="1d94e-106">이는 두 PQRS 사이의 패리티 차이를 평가 하기 위한 제어 비트 목록을 계산 합니다. 짝수의 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="1d94e-106">This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.</span></span>

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a><span data-ttu-id="1d94e-107">입력</span><span class="sxs-lookup"><span data-stu-id="1d94e-107">Input</span></span>

### <a name="prevfermionicterm--int"></a><span data-ttu-id="1d94e-108">prevFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1d94e-108">prevFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="nextfermionicterm--int"></a><span data-ttu-id="1d94e-109">nextFermionicTerm: [Int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1d94e-109">nextFermionicTerm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--intbool"></a><span data-ttu-id="1d94e-110">Output: ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span><span class="sxs-lookup"><span data-stu-id="1d94e-110">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Bool](xref:microsoft.quantum.lang-ref.bool)[])</span></span>



## <a name="remarks"></a><span data-ttu-id="1d94e-111">설명</span><span class="sxs-lookup"><span data-stu-id="1d94e-111">Remarks</span></span>

<span data-ttu-id="1d94e-112">여기서는 용어 길이가 짝수 라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d94e-112">This assumes that the length of terms is even.</span></span>
<span data-ttu-id="1d94e-113">두 용어 사이의 패리티 차이에 대 한 컨트롤 목록을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d94e-113">Computes list of controls for parity difference between any two terms.</span></span>
<span data-ttu-id="1d94e-114">여기서는 입력 목록이 오름차순으로 정렬 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d94e-114">This assumes that the input lists is sorted in ascending order.</span></span>