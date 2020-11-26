---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: BoolArrayAsPauli 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: 8e7088ec3918165d7b2afb1056a8319c6fb17796
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214282"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="81708-102">BoolArrayAsPauli 함수</span><span class="sxs-lookup"><span data-stu-id="81708-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="81708-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="81708-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="81708-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81708-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81708-105">비트 문자열이 지정 된 경우 단일 수준 비트 Pauli 연산자의 배열로 표시 되는 다중 값 비트 Pauli 연산자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="81708-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="81708-106">입력</span><span class="sxs-lookup"><span data-stu-id="81708-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="81708-107">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="81708-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="81708-108">에 적용 되는 pauli 연산자 `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="81708-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="81708-109">bitApply: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="81708-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="81708-110">bit가이 값 이면 Pauli를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81708-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="81708-111">bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="81708-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="81708-112">부울 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="81708-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="81708-113">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="81708-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="81708-114">설명</span><span class="sxs-lookup"><span data-stu-id="81708-114">Remarks</span></span>

<span data-ttu-id="81708-115">부울 배열과 퀀텀 레지스터의 길이는 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81708-115">The Boolean array and the quantum register must be of equal length.</span></span>