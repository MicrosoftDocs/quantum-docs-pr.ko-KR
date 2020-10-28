---
uid: Microsoft.Quantum.Canon._MultiplexOperationsFromGenerator
title: _MultiplexOperationsFromGenerator 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: _MultiplexOperationsFromGenerator
qsharp.summary: Implementation step of `MultiplexOperationsFromGenerator`.
ms.openlocfilehash: 17d8f3e9b800e26a00969418ca061e3ea1d97682
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718508"
---
# <a name="_multiplexoperationsfromgenerator-operation"></a><span data-ttu-id="a6076-102">_MultiplexOperationsFromGenerator 작업</span><span class="sxs-lookup"><span data-stu-id="a6076-102">_MultiplexOperationsFromGenerator operation</span></span>

<span data-ttu-id="a6076-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a6076-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a6076-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a6076-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a6076-105">의 구현 단계입니다 `MultiplexOperationsFromGenerator` .</span><span class="sxs-lookup"><span data-stu-id="a6076-105">Implementation step of `MultiplexOperationsFromGenerator`.</span></span>

```qsharp
operation _MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, Int, (Int -> ('T => Unit is Adj + Ctl))), auxiliary : Qubit[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="a6076-106">입력</span><span class="sxs-lookup"><span data-stu-id="a6076-106">Input</span></span>

### <a name="unitarygenerator--intintint---t--unit-adj--ctl"></a><span data-ttu-id="a6076-107">Unit Arygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span><span class="sxs-lookup"><span data-stu-id="a6076-107">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>




### <a name="auxiliary--qubit"></a><span data-ttu-id="a6076-108">보조: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a6076-108">auxiliary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>




### <a name="index--littleendian"></a><span data-ttu-id="a6076-109">인덱스: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a6076-109">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>




### <a name="target--t"></a><span data-ttu-id="a6076-110">대상: ' '</span><span class="sxs-lookup"><span data-stu-id="a6076-110">target : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="a6076-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a6076-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a6076-112">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a6076-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a6076-113">없습니다</span><span class="sxs-lookup"><span data-stu-id="a6076-113">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="a6076-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a6076-114">See Also</span></span>

- [<span data-ttu-id="a6076-115">MultiplexOperationsFromGenerator입니다.</span><span class="sxs-lookup"><span data-stu-id="a6076-115">Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)