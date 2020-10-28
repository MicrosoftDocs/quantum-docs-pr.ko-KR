---
uid: Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian
title: LittleEndianAsBigEndian 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndianAsBigEndian
qsharp.summary: Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: 8c2e6150a839bb0cd4c311c821b78a080288cd22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721021"
---
# <a name="littleendianasbigendian-function"></a><span data-ttu-id="f5c72-102">LittleEndianAsBigEndian 함수</span><span class="sxs-lookup"><span data-stu-id="f5c72-102">LittleEndianAsBigEndian function</span></span>

<span data-ttu-id="f5c72-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f5c72-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f5c72-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f5c72-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f5c72-105">에서 `LittleEndian` `BigEndian` 의 비트 순서를 반대로 하 여이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5c72-105">Converts a `LittleEndian` qubit register to a `BigEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function LittleEndianAsBigEndian (input : Microsoft.Quantum.Arithmetic.LittleEndian) : Microsoft.Quantum.Arithmetic.BigEndian
```


## <a name="input"></a><span data-ttu-id="f5c72-106">입력</span><span class="sxs-lookup"><span data-stu-id="f5c72-106">Input</span></span>

### <a name="input--littleendian"></a><span data-ttu-id="f5c72-107">입력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f5c72-107">input : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f5c72-108">형식에서의 `LittleEndian` 형식 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="f5c72-108">Qubit register in `LittleEndian` format.</span></span>



## <a name="output--bigendian"></a><span data-ttu-id="f5c72-109">출력:가 중 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="f5c72-109">Output : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="f5c72-110">형식에서의 `BigEndian` 형식 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="f5c72-110">Qubit register in `BigEndian` format.</span></span>