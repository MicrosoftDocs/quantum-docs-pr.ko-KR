---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: EmbedPauli 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: c78406aa4557834ac2bb40cf1847696d075e5135
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716199"
---
# <a name="embedpauli-function"></a><span data-ttu-id="32a78-102">EmbedPauli 함수</span><span class="sxs-lookup"><span data-stu-id="32a78-102">EmbedPauli function</span></span>

<span data-ttu-id="32a78-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="32a78-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="32a78-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="32a78-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="32a78-105">단일 기능 비트를 지정 하는 경우 해당 인덱스 및 다른 모든 인덱스에서 지정 된 단일 수준 비트 연산자를 사용 하 여 다중 값 비트 Pauli 연산자를 반환 합니다 `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="32a78-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="32a78-106">입력</span><span class="sxs-lookup"><span data-stu-id="32a78-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="32a78-107">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="32a78-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="32a78-108">지정 된 위치에 배치 되는 단일의 비트 Pauli 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="32a78-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="32a78-109">위치: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="32a78-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="32a78-110">`output[location] == pauli`이 함수의 출력 인 인덱스입니다 `output` .</span><span class="sxs-lookup"><span data-stu-id="32a78-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="32a78-111">n: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="32a78-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="32a78-112">반환 될 배열의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="32a78-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="32a78-113">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="32a78-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>
