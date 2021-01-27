---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: PhaseLittleEndian 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: 59df1db31090f875ccd261fe6cc43995ba57b963
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842994"
---
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="26479-102">PhaseLittleEndian 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="26479-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="26479-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="26479-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="26479-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26479-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26479-105">QFT 기반의 작은 endian 부호 없는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="26479-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="26479-106">예를 들어 $ \ket{x} $가 계산을 기준으로 하는 정수 $x $의 작은 endian 인코딩이 면 $ \operatorname{QFTLE} \ket{x} $는 QFT의 $x $의 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="26479-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="26479-107">설명</span><span class="sxs-lookup"><span data-stu-id="26479-107">Remarks</span></span>

<span data-ttu-id="26479-108">`PhaseLittleEndian`설명서에서와 같이 축약 `PhaseLE` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26479-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="26479-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="26479-109">See Also</span></span>

- [<span data-ttu-id="26479-110">Microsoft. 양자. QFT</span><span class="sxs-lookup"><span data-stu-id="26479-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="26479-111">QFTLE입니다.</span><span class="sxs-lookup"><span data-stu-id="26479-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)