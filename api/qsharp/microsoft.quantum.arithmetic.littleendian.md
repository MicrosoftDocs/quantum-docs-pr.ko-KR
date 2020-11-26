---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: LittleEndian 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: 2a00e499bf59e6d22a774706331737461e8e95e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222782"
---
# <a name="littleendian-user-defined-type"></a><span data-ttu-id="6b729-102">LittleEndian 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="6b729-102">LittleEndian user defined type</span></span>

<span data-ttu-id="6b729-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6b729-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6b729-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b729-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b729-105">부호 없는 정수를 거의 endian 순서로 인코딩하는 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="6b729-105">Register that encodes an unsigned integer in little-endian order.</span></span> <span data-ttu-id="6b729-106">인덱스가 있는 이상 비트는 `0` 부호 없는 정수의 최하위 비트를 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="6b729-106">The qubit with index `0` encodes the lowest bit of an unsigned integer.</span></span>

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a><span data-ttu-id="6b729-107">설명</span><span class="sxs-lookup"><span data-stu-id="6b729-107">Remarks</span></span>

<span data-ttu-id="6b729-108">`LittleEndian`설명서에서와 같이 축약 `LE` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b729-108">We abbreviate `LittleEndian` as `LE` in the documentation.</span></span>