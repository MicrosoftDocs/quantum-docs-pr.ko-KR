---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: BoolArrayAsPauli 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c5ef71322dae248fc2c6b1db3adf891de7d72488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713602"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="f2d47-102">BoolArrayAsPauli 함수</span><span class="sxs-lookup"><span data-stu-id="f2d47-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="f2d47-103">네임 스페이스: [Microsoft 양자 변환](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="f2d47-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="f2d47-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f2d47-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f2d47-105">비트 문자열이 지정 된 경우 단일 수준 비트 Pauli 연산자의 배열로 표시 되는 다중 값 비트 Pauli 연산자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d47-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="f2d47-106">입력</span><span class="sxs-lookup"><span data-stu-id="f2d47-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="f2d47-107">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="f2d47-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="f2d47-108">에 적용 되는 pauli 연산자 `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="f2d47-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="f2d47-109">bitApply: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f2d47-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f2d47-110">bit가이 값 이면 Pauli를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d47-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="f2d47-111">bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="f2d47-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="f2d47-112">부울 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f2d47-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="f2d47-113">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="f2d47-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="f2d47-114">설명</span><span class="sxs-lookup"><span data-stu-id="f2d47-114">Remarks</span></span>

<span data-ttu-id="f2d47-115">부울 배열과 퀀텀 레지스터의 길이는 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d47-115">The Boolean array and the quantum register must be of equal length.</span></span>