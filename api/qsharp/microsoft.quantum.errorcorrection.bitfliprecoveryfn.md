---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: BitFlipRecoveryFn 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: dad90475b2506187282825e143b11adc5120f453
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712496"
---
# <a name="bitfliprecoveryfn-function"></a><span data-ttu-id="c2466-102">BitFlipRecoveryFn 함수</span><span class="sxs-lookup"><span data-stu-id="c2466-102">BitFlipRecoveryFn function</span></span>

<span data-ttu-id="c2466-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="c2466-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="c2466-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2466-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2466-105">⟦ 3, 1, 1 ⟧ 비트 대칭 코드에 대 한 테이블 조회에 지정 된 증후군 측정에 대 한 복구 Pauli 작업에 대 한 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2466-105">Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.</span></span>

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="c2466-106">출력: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="c2466-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="c2466-107">`RecoveryFn`증후군 측정값을 사용 하 `Result[]` 고 `Pauli[]` 검색 된 오류를 수정 하는 작업을 반환 하는 형식의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2466-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2466-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c2466-108">See Also</span></span>

- [<span data-ttu-id="c2466-109">Microsoft 양자를 수정 합니다. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="c2466-109">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)