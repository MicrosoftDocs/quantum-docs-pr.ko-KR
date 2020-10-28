---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: LittleEndian 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: fd2744a8372793ad01d1391c035c64de1264d2f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721045"
---
# <a name="littleendian-user-defined-type"></a><span data-ttu-id="6bda3-102">LittleEndian 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="6bda3-102">LittleEndian user defined type</span></span>

<span data-ttu-id="6bda3-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6bda3-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6bda3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6bda3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6bda3-105">부호 없는 정수를 거의 endian 순서로 인코딩하는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="6bda3-105">Register that encodes an unsigned integer in little-endian order.</span></span> <span data-ttu-id="6bda3-106">인덱스가 있는 이상 비트는 `0` 부호 없는 정수의 최하위 비트를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="6bda3-106">The qubit with index `0` encodes the lowest bit of an unsigned integer.</span></span>

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="6bda3-107">설명</span><span class="sxs-lookup"><span data-stu-id="6bda3-107">Remarks</span></span>

<span data-ttu-id="6bda3-108">`LittleEndian`설명서에서와 같이 축약 `LE` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bda3-108">We abbreviate `LittleEndian` as `LE` in the documentation.</span></span>