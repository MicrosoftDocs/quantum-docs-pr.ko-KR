---
uid: Microsoft.Quantum.Math.InverseModL
title: InverseModL 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e7cb9e98cb0635c50162611f6a52c56027d4a5eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723630"
---
# <a name="inversemodl-function"></a><span data-ttu-id="8d003-102">InverseModL 함수</span><span class="sxs-lookup"><span data-stu-id="8d003-102">InverseModL function</span></span>

<span data-ttu-id="8d003-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="8d003-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="8d003-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8d003-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8d003-105">$A \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $과 같은 $b $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d003-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="8d003-106">입력</span><span class="sxs-lookup"><span data-stu-id="8d003-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="8d003-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="8d003-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="8d003-108">반전 되는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="8d003-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="8d003-109">모듈러스: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="8d003-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="8d003-110">숫자의 반전에 따른 모듈러스입니다.</span><span class="sxs-lookup"><span data-stu-id="8d003-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="8d003-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="8d003-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="8d003-112">정수 $b $ $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $입니다.</span><span class="sxs-lookup"><span data-stu-id="8d003-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>