---
uid: Microsoft.Quantum.Math.InverseModI
title: InverseModI 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 6efc9da5f5ebb64065a90e749daa629dc2dce9cf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723637"
---
# <a name="inversemodi-function"></a><span data-ttu-id="50e42-102">InverseModI 함수</span><span class="sxs-lookup"><span data-stu-id="50e42-102">InverseModI function</span></span>

<span data-ttu-id="50e42-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="50e42-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="50e42-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="50e42-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="50e42-105">$A \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $과 같은 $b $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="50e42-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="50e42-106">입력</span><span class="sxs-lookup"><span data-stu-id="50e42-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="50e42-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="50e42-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="50e42-108">반전 되는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="50e42-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="50e42-109">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="50e42-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="50e42-110">숫자의 반전에 따른 모듈러스입니다.</span><span class="sxs-lookup"><span data-stu-id="50e42-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="50e42-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="50e42-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="50e42-112">정수 $b $ $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $입니다.</span><span class="sxs-lookup"><span data-stu-id="50e42-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>