---
uid: Microsoft.Quantum.Math.ComplexPolar
title: ComplexPolar 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 0c18c3f02cb036f22a68b6e4b46fd19049dc34cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709647"
---
# <a name="complexpolar-user-defined-type"></a><span data-ttu-id="46397-102">ComplexPolar 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="46397-102">ComplexPolar user defined type</span></span>

<span data-ttu-id="46397-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="46397-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="46397-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46397-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46397-105">극좌표 형식의 복소수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46397-105">Represents a complex number in polar form.</span></span>

<span data-ttu-id="46397-106">복소수의 극좌표 표현은 $c = r e ^ {i t} $입니다.</span><span class="sxs-lookup"><span data-stu-id="46397-106">The polar representation of a complex number is $c=r e^{i t}$.</span></span>

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a><span data-ttu-id="46397-107">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="46397-107">Named Items</span></span>

### <a name="magnitude--double"></a><span data-ttu-id="46397-108">크기: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="46397-108">Magnitude : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="46397-109">$C $의 \ge $0 $r 절대값입니다.</span><span class="sxs-lookup"><span data-stu-id="46397-109">The absolute value $r \ge 0$ of $c$.</span></span>
### <a name="argument--double"></a><span data-ttu-id="46397-110">인수: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="46397-110">Argument : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="46397-111">$C $의 단계 $t \in \mathbb R $</span><span class="sxs-lookup"><span data-stu-id="46397-111">The phase $t \in \mathbb R$ of $c$.</span></span>