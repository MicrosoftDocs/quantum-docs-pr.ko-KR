---
uid: Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian
title: BigEndianAsLittleEndian 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndianAsLittleEndian
qsharp.summary: Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: cb4cf68753468952c7541fae23250ed1fd1914f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843379"
---
# <a name="bigendianaslittleendian-function"></a><span data-ttu-id="aa3a1-102">BigEndianAsLittleEndian 함수</span><span class="sxs-lookup"><span data-stu-id="aa3a1-102">BigEndianAsLittleEndian function</span></span>

<span data-ttu-id="aa3a1-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="aa3a1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="aa3a1-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa3a1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa3a1-105">에서 `BigEndian` `LittleEndian` 의 비트 순서를 반대로 하 여이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa3a1-105">Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function BigEndianAsLittleEndian (input : Microsoft.Quantum.Arithmetic.BigEndian) : Microsoft.Quantum.Arithmetic.LittleEndian
```


## <a name="input"></a><span data-ttu-id="aa3a1-106">입력</span><span class="sxs-lookup"><span data-stu-id="aa3a1-106">Input</span></span>

### <a name="input--bigendian"></a><span data-ttu-id="aa3a1-107">입력:가 나 [endian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="aa3a1-107">input : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="aa3a1-108">형식에서의 `BigEndian` 형식 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="aa3a1-108">Qubit register in `BigEndian` format.</span></span>



## <a name="output--littleendian"></a><span data-ttu-id="aa3a1-109">출력: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="aa3a1-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="aa3a1-110">형식에서의 `LittleEndian` 형식 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="aa3a1-110">Qubit register in `LittleEndian` format.</span></span>