---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: CopyMostSignificantBit 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843263"
---
# <a name="copymostsignificantbit-operation"></a><span data-ttu-id="5aafa-102">CopyMostSignificantBit 작업</span><span class="sxs-lookup"><span data-stu-id="5aafa-102">CopyMostSignificantBit operation</span></span>

<span data-ttu-id="5aafa-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5aafa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5aafa-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5aafa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5aafa-105">`from`부호 없는 정수를 나타내는 값 비트 레지스터의 가장 중요 한 비트를 해당 비트에 복사 합니다 `target` .</span><span class="sxs-lookup"><span data-stu-id="5aafa-105">Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.</span></span>

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="5aafa-106">입력</span><span class="sxs-lookup"><span data-stu-id="5aafa-106">Input</span></span>

### <a name="from--littleendian"></a><span data-ttu-id="5aafa-107">시작: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5aafa-107">from : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5aafa-108">상위 비트가 복사 되는 부호 없는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="5aafa-108">The unsigned integer from which the highest bit is copied from.</span></span>
<span data-ttu-id="5aafa-109">정수는 작은 endian 형식으로 인코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="5aafa-109">the integer is encoded in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="5aafa-110">대상: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5aafa-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5aafa-111">가장 높은 비트를 복사할 때 기준이 되는 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="5aafa-111">The qubit in which the highest bit is being copied.</span></span> <span data-ttu-id="5aafa-112">비트 인코딩은 계산 기준입니다.</span><span class="sxs-lookup"><span data-stu-id="5aafa-112">The bit encoding is in computational basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5aafa-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5aafa-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="5aafa-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5aafa-114">See Also</span></span>

- [<span data-ttu-id="5aafa-115">LittleEndian.</span><span class="sxs-lookup"><span data-stu-id="5aafa-115">Microsoft.Quantum.Arithmetic.LittleEndian</span></span>](xref:Microsoft.Quantum.Arithmetic.LittleEndian)