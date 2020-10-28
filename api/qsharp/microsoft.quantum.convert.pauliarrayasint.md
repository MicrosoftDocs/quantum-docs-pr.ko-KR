---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: PauliArrayAsInt 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713371"
---
# <a name="pauliarrayasint-function"></a><span data-ttu-id="45948-102">PauliArrayAsInt 함수</span><span class="sxs-lookup"><span data-stu-id="45948-102">PauliArrayAsInt function</span></span>

<span data-ttu-id="45948-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="45948-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="45948-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="45948-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="45948-105">단일가 나 비트 Pauli 연산자의 배열로 표현 되는 다중 기능 비트 Pauli 연산자를 정수로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="45948-105">Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.</span></span>

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="45948-106">입력</span><span class="sxs-lookup"><span data-stu-id="45948-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="45948-107">paulis: [Paulis](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="45948-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="45948-108">최대 31 개의 단일 수준 Pauli 연산자의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="45948-108">An array of at most 31 single-qubit Pauli operators.</span></span>



## <a name="output--int"></a><span data-ttu-id="45948-109">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="45948-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="45948-110">아래에서 설명 하는 고유 하 게 식별 하는 정수 `paulis` 입니다.</span><span class="sxs-lookup"><span data-stu-id="45948-110">An integer uniquely identifying `paulis`, as described below.</span></span>

## <a name="remarks"></a><span data-ttu-id="45948-111">설명</span><span class="sxs-lookup"><span data-stu-id="45948-111">Remarks</span></span>

<span data-ttu-id="45948-112">각 Pauli 연산자는 두 비트를 사용 하 여 인코딩할 수 있습니다. $ $ \begin{align} \boldone \maps00, \쿼드 X \maps01, \쿼드 Y \maps11, \쿼드 Z \maps10.</span><span class="sxs-lookup"><span data-stu-id="45948-112">Each Pauli operator can be encoded using two bits: $$ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span></span>
<span data-ttu-id="45948-113">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="45948-113">\end{align} $$</span></span>

<span data-ttu-id="45948-114">Pauli 연산자의 배열이 지정 된 `[P0, ..., Pn]` 경우이 함수는 각 Pauli 연산자의 매핑을 빅 endian 순서로 연결 하 여 이진 확장이 형성 된 정수를 반환 `bits(Pn) ... bits(P0)` 합니다.</span><span class="sxs-lookup"><span data-stu-id="45948-114">Given an array of Pauli operators `[P0, ..., Pn]`, this function returns an integer with binary expansion formed by concatenating the mappings of each Pauli operator in big-endian order `bits(Pn) ... bits(P0)`.</span></span>