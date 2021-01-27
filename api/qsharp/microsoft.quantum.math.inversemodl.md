---
uid: Microsoft.Quantum.Math.InverseModL
title: InverseModL 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e09c9da500889dfcb514d0a02dec957bfaa70e1c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851400"
---
# <a name="inversemodl-function"></a><span data-ttu-id="c6002-102">InverseModL 함수</span><span class="sxs-lookup"><span data-stu-id="c6002-102">InverseModL function</span></span>

<span data-ttu-id="c6002-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="c6002-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="c6002-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c6002-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c6002-105">$A \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $과 같은 $b $를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6002-105">Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="c6002-106">입력</span><span class="sxs-lookup"><span data-stu-id="c6002-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="c6002-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="c6002-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="c6002-108">반전 되는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="c6002-108">The number being inverted</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="c6002-109">모듈러스: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="c6002-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="c6002-110">숫자의 반전에 따른 모듈러스입니다.</span><span class="sxs-lookup"><span data-stu-id="c6002-110">The modulus according to which the numbers are inverted</span></span>



## <a name="output--bigint"></a><span data-ttu-id="c6002-111">출력: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="c6002-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="c6002-112">정수 $b $ $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $입니다.</span><span class="sxs-lookup"><span data-stu-id="c6002-112">Integer $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.</span></span>