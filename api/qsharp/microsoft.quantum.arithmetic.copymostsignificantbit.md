---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: CopyMostSignificantBit 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 02119103fa7b5776f0e1681535115e0773a34c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721213"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="c39bb-102">CopyMostSignificantBit 작업</span><span class="sxs-lookup"><span data-stu-id="c39bb-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="c39bb-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c39bb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c39bb-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c39bb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c39bb-105">`from`부호 없는 정수를 나타내는 값 비트 레지스터의 가장 중요 한 비트를 해당 비트에 복사 합니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="c39bb-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="c39bb-106">입력</span><span class="sxs-lookup"><span data-stu-id="c39bb-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="c39bb-107">시작: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c39bb-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c39bb-108">상위 비트가 복사 되는 부호 없는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="c39bb-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="c39bb-109">정수는 작은 endian 형식으로 인코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="c39bb-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="c39bb-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c39bb-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c39bb-111">가장 높은 비트를 복사할 때 기준이 되는 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="c39bb-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="c39bb-112">비트 인코딩은 계산 기준입니다.</span><span class="sxs-lookup"><span data-stu-id="c39bb-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c39bb-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c39bb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="c39bb-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c39bb-114">See Also</span></span>

- [<span data-ttu-id="c39bb-115">LittleEndian.</span><span class="sxs-lookup"><span data-stu-id="c39bb-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)