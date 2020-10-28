---
uid: Microsoft.Quantum.ErrorCorrection.RecoveryFn
title: RecoveryFn 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoveryFn
qsharp.summary: Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.
ms.openlocfilehash: 6f4db7312fadbd8ca4c6b8533f78c2c5a886f30e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712195"
---
# <a name="recoveryfn-user-defined-type"></a><span data-ttu-id="49f2a-102">RecoveryFn 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="49f2a-102">RecoveryFn user defined type</span></span>

<span data-ttu-id="49f2a-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="49f2a-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="49f2a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="49f2a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="49f2a-105">증후군 오류를 `Pauli[]` 검색 된 오류를 해결 하는 일련의 작업에 매핑하는 함수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="49f2a-105">Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.</span></span>

```qsharp

newtype RecoveryFn = ((Microsoft.Quantum.ErrorCorrection.Syndrome -> Pauli[]));
```

