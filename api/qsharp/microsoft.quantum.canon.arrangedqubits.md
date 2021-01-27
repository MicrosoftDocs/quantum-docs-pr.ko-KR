---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: ArrangedQubits 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 07a4ed5fe99dedb333246f7161d157dcd01a01da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841070"
---
# <a name="arrangedqubits-function"></a><span data-ttu-id="74451-102">ArrangedQubits 함수</span><span class="sxs-lookup"><span data-stu-id="74451-102">ArrangedQubits function</span></span>

<span data-ttu-id="74451-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="74451-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="74451-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="74451-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="74451-105">인덱스에 따라 컨트롤, 대상 및 도우미의 정렬</span><span class="sxs-lookup"><span data-stu-id="74451-105">Arrange control, target, and helper qubits according to an index</span></span>

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a><span data-ttu-id="74451-106">설명</span><span class="sxs-lookup"><span data-stu-id="74451-106">Description</span></span>

<span data-ttu-id="74451-107">인덱스 0에서 target을 사용 하 고 인덱스 2 ^ i에서 컨트롤 i를 사용 하 여 원하는 비트 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="74451-107">Returns a Qubit array with target at index 0, and control i at index 2^i.</span></span>  <span data-ttu-id="74451-108">도우미는 배열의 다른 모든 위치에 삽입 됩니다.</span><span class="sxs-lookup"><span data-stu-id="74451-108">The helper qubits are inserted to all other positions in the array.</span></span>

## <a name="input"></a><span data-ttu-id="74451-109">입력</span><span class="sxs-lookup"><span data-stu-id="74451-109">Input</span></span>

### <a name="controls--qubit"></a><span data-ttu-id="74451-110">컨트롤: [이상](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="74451-110">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="target--qubit"></a><span data-ttu-id="74451-111">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="74451-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>




### <a name="helper--qubit"></a><span data-ttu-id="74451-112">도우미:의 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="74451-112">helper : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--qubit"></a><span data-ttu-id="74451-113">출력: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="74451-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

