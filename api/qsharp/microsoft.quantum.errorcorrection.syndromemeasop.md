---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: SyndromeMeasOp 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 65e47d82546b1df0beec2c00f435d3e7a28e6ae6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200257"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="08f06-102">SyndromeMeasOp 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="08f06-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="08f06-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="08f06-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="08f06-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="08f06-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="08f06-105">오류 수정 코드 블록의 증후군을 측정 하는 데 사용 되는 작업을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a><span data-ttu-id="08f06-106">설명</span><span class="sxs-lookup"><span data-stu-id="08f06-106">Remarks</span></span>

<span data-ttu-id="08f06-107">시그니처는 `(LogicalRegister => Syndrome)` 의 이상 값에 대해 공동으로 작동 하는 작업을 나타내며 일부 보조의 경우에는 보조 비트를 측정 하 여 `LogicalRegister` `Syndrome` 이러한 측정의을 나타내는 값을 추출 합니다 `Result[]` .</span><span class="sxs-lookup"><span data-stu-id="08f06-107">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="08f06-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="08f06-108">See Also</span></span>

- [<span data-ttu-id="08f06-109">Microsoft 양자를 수정 합니다. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="08f06-109">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="08f06-110">증후군를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-110">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)