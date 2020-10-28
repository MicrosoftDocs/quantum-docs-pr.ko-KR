---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBEGeneratorSystem
title: OptimizedBEGeneratorSystem 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedBEGeneratorSystem
qsharp.summary: Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.
ms.openlocfilehash: 06d13a8a64a3c572821ec97f8776d6f1dbe4a4ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713938"
---
# <a name="optimizedbegeneratorsystem-user-defined-type"></a><span data-ttu-id="af594-102">OptimizedBEGeneratorSystem 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="af594-102">OptimizedBEGeneratorSystem user defined type</span></span>

<span data-ttu-id="af594-103">네임 스페이스: [JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="af594-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="af594-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="af594-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="af594-105">정수에 지정 된 정수에 대 한 데이터를 반환 하는 함수입니다 .이 함수는 `OptimizedBETermIndex` 첫 번째에 있는 `n` `n` 용어 수와 `Int` 에 있는 모든 용어 계수의 절대값 합계와 함께 사용 `Double` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af594-105">Function that returns `OptimizedBETermIndex` data for term `n` given an integer `n`, together with the number of terms in the first `Int` and the sum of absolute-values of all term coefficients in the `Double`.</span></span>

```qsharp

newtype OptimizedBEGeneratorSystem = (Int, Double, (Int -> Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex));
```

