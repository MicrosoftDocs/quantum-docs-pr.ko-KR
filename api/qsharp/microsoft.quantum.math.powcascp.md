---
uid: Microsoft.Quantum.Math.PowCAsCP
title: PowCAsCP 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PowCAsCP
qsharp.summary: Internal. Since it is easiest to define the power of two complex numbers in cartesian form as returning in polar form, we define that here, then convert as needed.
ms.openlocfilehash: fb629f360e4b19715e406d4a4f4fae7a31e81736
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847063"
---
# <a name="powcascp-function"></a><span data-ttu-id="baada-102">PowCAsCP 함수</span><span class="sxs-lookup"><span data-stu-id="baada-102">PowCAsCP function</span></span>

<span data-ttu-id="baada-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="baada-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="baada-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="baada-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="baada-105">내부에서 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="baada-105">Internal.</span></span> <span data-ttu-id="baada-106">극좌표 형 형식으로 반환 하는 것 처럼 두 복소수를 데카르트 형식으로 정의 하는 것이 가장 간단 하기 때문에 여기에서 정의한 다음 필요에 따라 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="baada-106">Since it is easiest to define the power of two complex numbers in cartesian form as returning in polar form, we define that here, then convert as needed.</span></span>

```qsharp
function PowCAsCP (base_ : Microsoft.Quantum.Math.Complex, power : Microsoft.Quantum.Math.Complex) : Microsoft.Quantum.Math.ComplexPolar
```


## <a name="input"></a><span data-ttu-id="baada-107">입력</span><span class="sxs-lookup"><span data-stu-id="baada-107">Input</span></span>

### <a name="base_--complex"></a><span data-ttu-id="baada-108">base_: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="baada-108">base_ : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>




### <a name="power--complex"></a><span data-ttu-id="baada-109">전원: [복합](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="baada-109">power : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>





## <a name="output--complexpolar"></a><span data-ttu-id="baada-110">출력: [Complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="baada-110">Output : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

