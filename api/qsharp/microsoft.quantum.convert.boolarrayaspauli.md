---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: BoolArrayAsPauli 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c11ca05ad8a939d704547c65a8e8a6537d0df4b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834244"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="88176-102">BoolArrayAsPauli 함수</span><span class="sxs-lookup"><span data-stu-id="88176-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="88176-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="88176-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="88176-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="88176-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="88176-105">비트 문자열이 지정 된 경우 단일 수준 비트 Pauli 연산자의 배열로 표시 되는 다중 값 비트 Pauli 연산자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88176-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="88176-106">입력</span><span class="sxs-lookup"><span data-stu-id="88176-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="88176-107">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="88176-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="88176-108">에 적용 되는 pauli 연산자 `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="88176-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="88176-109">bitApply: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="88176-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="88176-110">bit가이 값 이면 Pauli를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="88176-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="88176-111">bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="88176-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="88176-112">부울 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="88176-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="88176-113">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="88176-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="88176-114">설명</span><span class="sxs-lookup"><span data-stu-id="88176-114">Remarks</span></span>

<span data-ttu-id="88176-115">부울 배열과 퀀텀 레지스터의 길이는 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88176-115">The Boolean array and the quantum register must be of equal length.</span></span>