---
uid: Microsoft.Quantum.ErrorCorrection.RecoveryFn
title: RecoveryFn 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoveryFn
qsharp.summary: Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.
ms.openlocfilehash: 7e8afa37e6225239ae7cafa1f48377a97c43297d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825095"
---
# <a name="recoveryfn-user-defined-type"></a><span data-ttu-id="a5f8e-102">RecoveryFn 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="a5f8e-102">RecoveryFn user defined type</span></span>

<span data-ttu-id="a5f8e-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a5f8e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a5f8e-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5f8e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5f8e-105">증후군 오류를 `Pauli[]` 검색 된 오류를 해결 하는 일련의 작업에 매핑하는 함수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f8e-105">Type for function that maps an error syndrome to a sequence of `Pauli[]` operations that correct the detected error.</span></span>

```qsharp

newtype RecoveryFn = ((Microsoft.Quantum.ErrorCorrection.Syndrome -> Pauli[]));
```

