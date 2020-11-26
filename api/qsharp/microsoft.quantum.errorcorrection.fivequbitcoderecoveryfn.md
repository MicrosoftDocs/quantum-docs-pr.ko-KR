---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: Fivkebitcoderec과잉 Yfn 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 47e8a74d3631be2209537679ec9786a8dab63c58
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200784"
---
# <a name="fivequbitcoderecoveryfn-function"></a><span data-ttu-id="7990d-102">Fivkebitcoderec과잉 Yfn 함수</span><span class="sxs-lookup"><span data-stu-id="7990d-102">FiveQubitCodeRecoveryFn function</span></span>

<span data-ttu-id="7990d-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="7990d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="7990d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7990d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7990d-105">⟦ 5, 1, 3 ⟧ 퀀텀 코드에 대 한 테이블 조회에 따라 오류 증후군 측정값을 적절 한 오류 수정으로 매핑하는 함수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7990d-105">Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a><span data-ttu-id="7990d-106">출력: [Recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="7990d-106">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="7990d-107">`RecoveryFn`증후군 측정값을 사용 하 `Result[]` 고 `Pauli[]` 검색 된 오류를 수정 하는 연산자를 반환 하는 형식의 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="7990d-107">Function of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operators that corrects the detected error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7990d-108">설명</span><span class="sxs-lookup"><span data-stu-id="7990d-108">Remarks</span></span>

<span data-ttu-id="7990d-109">가중치 $1 $의 모든 오류를 반복 하 여 총 $3 \ 시간 5 = 15 $ 가능한 사소한 syndromes을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7990d-109">By iterating over all errors of weight $1$, we obtain a total of $3\times 5=15$ possible non-trivial syndromes.</span></span>
<span data-ttu-id="7990d-110">Id와 함께 오류 테이블과 해당 증후군이 작성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7990d-110">Together with the identity, a table of error and corresponding syndrome is built up.</span></span> <span data-ttu-id="7990d-111">5 비트 코드의 경우이 테이블은 $X \_ 1: (0, 0, 0, 1)로 지정 됩니다. X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0, 0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0, 0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ $X _i $ 및 $Z _i $ syndromes를 추가 하 여 _i $를 가져온 $Y.</span><span class="sxs-lookup"><span data-stu-id="7990d-111">For the 5 qubit code this table is given by: $X\_1: (0,0,0,1); X\_2: (1,0,0,0); X\_3: (1,1,0,0); X\_4: (0,1,1,0); X\_5: (0,0,1,1)$, $Z\_1: (1,0,1,0); Z\_2: (0,1,0,1); Z\_3: (0,0,1,0); Z\_4: (1,0,0,1); Z\_5: (0,1,0,0)$ with $Y_i$ obtained by adding the $X_i$ and $Z_i$ syndromes.</span></span> <span data-ttu-id="7990d-112">테이블 조회 복구의 순서는 bitvectors를 정수로 변환 하 여 제공 됩니다 (little endian 사용).</span><span class="sxs-lookup"><span data-stu-id="7990d-112">Note that the ordering in the table lookup recovery is given by converting the bitvectors to integers (using little endian).</span></span>

## <a name="see-also"></a><span data-ttu-id="7990d-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7990d-113">See Also</span></span>

- [<span data-ttu-id="7990d-114">Microsoft 양자를 수정 합니다. RecoveryFn</span><span class="sxs-lookup"><span data-stu-id="7990d-114">Microsoft.Quantum.ErrorCorrection.RecoveryFn</span></span>](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)