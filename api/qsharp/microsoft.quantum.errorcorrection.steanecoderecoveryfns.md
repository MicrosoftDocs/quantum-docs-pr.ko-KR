---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: SteaneCodeRecoveryFns 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 7395996e75c5a1c0c5d13f76d9ec76acae5683c7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200410"
---
# <a name="steanecoderecoveryfns-function"></a><span data-ttu-id="a411d-102">SteaneCodeRecoveryFns 함수</span><span class="sxs-lookup"><span data-stu-id="a411d-102">SteaneCodeRecoveryFns function</span></span>

<span data-ttu-id="a411d-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a411d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a411d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a411d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a411d-105">⟦ 7, 1, 3 ⟧ Steane 퀀텀 코드의 안정기 그룹에 결합 된 X 및 Z 부분을 위한 디코더입니다.</span><span class="sxs-lookup"><span data-stu-id="a411d-105">Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a><span data-ttu-id="a411d-106">출력: ([recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[recoveryfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span><span class="sxs-lookup"><span data-stu-id="a411d-106">Output : ([RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))</span></span>

<span data-ttu-id="a411d-107">`RecoveryFn`증후군 측정값을 사용 하 `Result[]` 고 `Pauli[]` 검색 된 오류를 수정 하는 작업을 반환 하는 형식의 함수 튜플입니다.</span><span class="sxs-lookup"><span data-stu-id="a411d-107">Tuple of functions of type `RecoveryFn` that takes a syndrome measurement `Result[]` and returns the `Pauli[]` operations that corrects the detected error.</span></span>

## <a name="see-also"></a><span data-ttu-id="a411d-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a411d-108">See Also</span></span>

- [<span data-ttu-id="a411d-109">SteaneCodeRecoveryX를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a411d-109">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="a411d-110">SteaneCodeRecoveryZ를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a411d-110">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)