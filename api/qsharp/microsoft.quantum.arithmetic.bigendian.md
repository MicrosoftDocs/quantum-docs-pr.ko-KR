---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: 이상 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 2f6ec9f83ac124ce9b06c278f8fda820c35c23aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843388"
---
# <a name="bigendian-user-defined-type"></a><span data-ttu-id="30c37-102">이상 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="30c37-102">BigEndian user defined type</span></span>

<span data-ttu-id="30c37-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="30c37-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="30c37-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30c37-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30c37-105">부호 없는 정수를 빅 endian 순서로 인코딩하는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="30c37-105">Register that encodes an unsigned integer in big-endian order.</span></span> <span data-ttu-id="30c37-106">인덱스를 사용 하는가 중 비트는 `0` 부호 없는 정수의 상위 비트를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="30c37-106">The qubit with index `0` encodes the highest bit of an unsigned integer.</span></span>

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="30c37-107">설명</span><span class="sxs-lookup"><span data-stu-id="30c37-107">Remarks</span></span>

<span data-ttu-id="30c37-108">`BigEndian`설명서에서와 같이 축약 `BE` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30c37-108">We abbreviate `BigEndian` as `BE` in the documentation.</span></span>