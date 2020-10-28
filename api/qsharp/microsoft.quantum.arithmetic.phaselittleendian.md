---
uid: Microsoft.Quantum.Arithmetic.PhaseLittleEndian
title: PhaseLittleEndian 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: PhaseLittleEndian
qsharp.summary: >-
  Little-endian unsigned integers in QFT basis.

  For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.
ms.openlocfilehash: f1f792d62004a2765d4e63870f5a41a4377b0d34
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92719732"
---
# <a name="phaselittleendian-user-defined-type"></a><span data-ttu-id="0a78e-102">PhaseLittleEndian 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="0a78e-102">PhaseLittleEndian user defined type</span></span>

<span data-ttu-id="0a78e-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0a78e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0a78e-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0a78e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0a78e-105">QFT 기반의 작은 endian 부호 없는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="0a78e-105">Little-endian unsigned integers in QFT basis.</span></span>

<span data-ttu-id="0a78e-106">예를 들어 $ \ket{x} $가 계산을 기준으로 하는 정수 $x $의 작은 endian 인코딩이 면 $ \operatorname{QFTLE} \ket{x} $는 QFT의 $x $의 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="0a78e-106">For example, if $\ket{x}$ is the little-endian encoding of the integer $x$ in the computational basis, then $\operatorname{QFTLE} \ket{x}$ is the encoding of $x$ in the QFT basis.</span></span>

```qsharp

newtype PhaseLittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="0a78e-107">설명</span><span class="sxs-lookup"><span data-stu-id="0a78e-107">Remarks</span></span>

<span data-ttu-id="0a78e-108">`PhaseLittleEndian`설명서에서와 같이 축약 `PhaseLE` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a78e-108">We abbreviate `PhaseLittleEndian` as `PhaseLE` in the documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a78e-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0a78e-109">See Also</span></span>

- [<span data-ttu-id="0a78e-110">Microsoft. 양자. QFT</span><span class="sxs-lookup"><span data-stu-id="0a78e-110">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)
- [<span data-ttu-id="0a78e-111">QFTLE입니다.</span><span class="sxs-lookup"><span data-stu-id="0a78e-111">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)