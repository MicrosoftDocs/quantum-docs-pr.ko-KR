---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: ApplyPauliFromBitString 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: cf4c99ec5134fac788cdd4c8a057258790152a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209063"
---
# <a name="applypaulifrombitstring-operation"></a><span data-ttu-id="49977-102">ApplyPauliFromBitString 작업</span><span class="sxs-lookup"><span data-stu-id="49977-102">ApplyPauliFromBitString operation</span></span>

<span data-ttu-id="49977-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="49977-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="49977-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49977-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49977-105">부울 배열의 해당 비트가 지정 된 입력과 일치 하는 경우 배열의 각 비트에 Pauli 연산자를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49977-105">Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.</span></span>

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="49977-106">입력</span><span class="sxs-lookup"><span data-stu-id="49977-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="49977-107">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="49977-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="49977-108">에 적용할 pauli 연산자 `qubits[idx]``bitsApply == bits[idx]`</span><span class="sxs-lookup"><span data-stu-id="49977-108">Pauli operator to apply to `qubits[idx]` where `bitsApply == bits[idx]`</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="49977-109">bitApply: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="49977-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="49977-110">bit가이 값인 경우 Pauli 적용</span><span class="sxs-lookup"><span data-stu-id="49977-110">apply Pauli if bit is this value</span></span>


### <a name="bits--bool"></a><span data-ttu-id="49977-111">bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="49977-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="49977-112">에서 작동 해야 하는 해당 고 비트를 지정 하는 부울 레지스터입니다. `qubits`</span><span class="sxs-lookup"><span data-stu-id="49977-112">Boolean register specifying which corresponding qubit in `qubits` should be operated on</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="49977-113">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="49977-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="49977-114">지정 된 Pauli 연산자를 선택적으로 적용할 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="49977-114">Quantum register on which to selectively apply the specified Pauli operator</span></span>



## <a name="output--unit"></a><span data-ttu-id="49977-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="49977-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="49977-116">설명</span><span class="sxs-lookup"><span data-stu-id="49977-116">Remarks</span></span>

<span data-ttu-id="49977-117">부울 배열과 퀀텀 레지스터의 길이는 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49977-117">The Boolean array and the quantum register must be of equal length.</span></span>