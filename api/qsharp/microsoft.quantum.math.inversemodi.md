---
uid: Microsoft.Quantum.Math.InverseModI
title: InverseModI 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModI
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: 474146e644bcd042e85b917bc43135a674bedce1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846881"
---
# <a name="inversemodi-function"></a><span data-ttu-id="d230d-102">InverseModI 함수</span><span class="sxs-lookup"><span data-stu-id="d230d-102">InverseModI function</span></span>

<span data-ttu-id="d230d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d230d-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d230d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d230d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d230d-105">$A \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $과 같은 $b $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d230d-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModI (a : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="d230d-106">입력</span><span class="sxs-lookup"><span data-stu-id="d230d-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="d230d-107">a: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d230d-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d230d-108">반전 되는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="d230d-108">The number being inverted</span></span>


### <a name="modulus--int"></a><span data-ttu-id="d230d-109">모듈러스: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d230d-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d230d-110">숫자의 반전에 따른 모듈러스입니다.</span><span class="sxs-lookup"><span data-stu-id="d230d-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--int"></a><span data-ttu-id="d230d-111">출력: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d230d-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d230d-112">정수 $b $ $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $입니다.</span><span class="sxs-lookup"><span data-stu-id="d230d-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>