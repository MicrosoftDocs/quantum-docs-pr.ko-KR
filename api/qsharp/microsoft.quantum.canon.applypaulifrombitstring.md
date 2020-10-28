---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: ApplyPauliFromBitString 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: 09754accb92c1339b781003e5722e3c8f5884e6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717809"
---
# <a name="applypaulifrombitstring-operation"></a><span data-ttu-id="5b358-102">ApplyPauliFromBitString 작업</span><span class="sxs-lookup"><span data-stu-id="5b358-102">ApplyPauliFromBitString operation</span></span>

<span data-ttu-id="5b358-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5b358-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5b358-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b358-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5b358-105">부울 배열의 해당 비트가 지정 된 입력과 일치 하는 경우 배열의 각 비트에 Pauli 연산자를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b358-105">Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.</span></span>

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5b358-106">입력</span><span class="sxs-lookup"><span data-stu-id="5b358-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="5b358-107">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="5b358-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="5b358-108">에 적용할 pauli 연산자 `qubits[idx]``bitsApply == bits[idx]`</span><span class="sxs-lookup"><span data-stu-id="5b358-108">Pauli operator to apply to `qubits[idx]` where `bitsApply == bits[idx]`</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="5b358-109">bitApply: [Bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5b358-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5b358-110">bit가이 값인 경우 Pauli 적용</span><span class="sxs-lookup"><span data-stu-id="5b358-110">apply Pauli if bit is this value</span></span>


### <a name="bits--bool"></a><span data-ttu-id="5b358-111">bits: [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="5b358-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="5b358-112">에서 작동 해야 하는 해당 고 비트를 지정 하는 부울 레지스터입니다. `qubits`</span><span class="sxs-lookup"><span data-stu-id="5b358-112">Boolean register specifying which corresponding qubit in `qubits` should be operated on</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5b358-113">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5b358-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5b358-114">지정 된 Pauli 연산자를 선택적으로 적용할 퀀텀 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="5b358-114">Quantum register on which to selectively apply the specified Pauli operator</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b358-115">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b358-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5b358-116">설명</span><span class="sxs-lookup"><span data-stu-id="5b358-116">Remarks</span></span>

<span data-ttu-id="5b358-117">부울 배열과 퀀텀 레지스터의 길이는 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b358-117">The Boolean array and the quantum register must be of equal length.</span></span>