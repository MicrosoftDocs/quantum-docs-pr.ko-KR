---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: EmbedPauli 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: 0e6a93e22ee495abcc44bdf522e7c72c0981308b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840529"
---
# <a name="embedpauli-function"></a><span data-ttu-id="f86b5-102">EmbedPauli 함수</span><span class="sxs-lookup"><span data-stu-id="f86b5-102">EmbedPauli function</span></span>

<span data-ttu-id="f86b5-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f86b5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f86b5-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f86b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f86b5-105">단일 기능 비트를 지정 하는 경우 해당 인덱스 및 다른 모든 인덱스에서 지정 된 단일 수준 비트 연산자를 사용 하 여 다중 값 비트 Pauli 연산자를 반환 합니다 `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="f86b5-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="f86b5-106">입력</span><span class="sxs-lookup"><span data-stu-id="f86b5-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="f86b5-107">pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="f86b5-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="f86b5-108">지정 된 위치에 배치 되는 단일의 비트 Pauli 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="f86b5-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="f86b5-109">위치: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f86b5-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f86b5-110">`output[location] == pauli`이 함수의 출력 인 인덱스입니다 `output` .</span><span class="sxs-lookup"><span data-stu-id="f86b5-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="f86b5-111">n: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f86b5-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f86b5-112">반환 될 배열의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="f86b5-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="f86b5-113">출력: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="f86b5-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="example"></a><span data-ttu-id="f86b5-114">예</span><span class="sxs-lookup"><span data-stu-id="f86b5-114">Example</span></span>

<span data-ttu-id="f86b5-115">배열을 가져오려면 다음을 `[PauliI, PauliI, PauliX, PauliI]` 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f86b5-115">To obtain the array `[PauliI, PauliI, PauliX, PauliI]`:</span></span>

```qsharp
EmbedPauli(PauliX, 2, 3);
```