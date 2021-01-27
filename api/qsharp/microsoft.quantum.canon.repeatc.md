---
uid: Microsoft.Quantum.Canon.RepeatC
title: RepeatC 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: efb820411be63352fc09ada2441a9140dd5575f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840255"
---
# <a name="repeatc-operation"></a><span data-ttu-id="a08a4-102">RepeatC 작업</span><span class="sxs-lookup"><span data-stu-id="a08a4-102">RepeatC operation</span></span>

<span data-ttu-id="a08a4-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a08a4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a08a4-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a08a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a08a4-105">지정 된 횟수 만큼 작업을 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="a08a4-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="a08a4-106">입력</span><span class="sxs-lookup"><span data-stu-id="a08a4-106">Input</span></span>

### <a name="op--tinput--unit--is-ctl"></a><span data-ttu-id="a08a4-107">op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="a08a4-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a08a4-108">반복적으로 호출 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a08a4-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="a08a4-109">nTimes: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a08a4-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a08a4-110">호출 하는 횟수 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a08a4-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="a08a4-111">입력: ' TInput</span><span class="sxs-lookup"><span data-stu-id="a08a4-111">input : 'TInput</span></span>

<span data-ttu-id="a08a4-112">에 전달 되는 입력 `op` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a08a4-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a08a4-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a08a4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a08a4-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a08a4-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="a08a4-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="a08a4-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="a08a4-116">예</span><span class="sxs-lookup"><span data-stu-id="a08a4-116">Example</span></span>

<span data-ttu-id="a08a4-117">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="a08a4-117">The following are equivalent:</span></span>

```qsharp
RepeatC(U, 17, target);
(BoundC(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="a08a4-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a08a4-118">See Also</span></span>

- [<span data-ttu-id="a08a4-119">Microsoft 양자 Many</span><span class="sxs-lookup"><span data-stu-id="a08a4-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="a08a4-120">Microsoft. 양자 반복</span><span class="sxs-lookup"><span data-stu-id="a08a4-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="a08a4-121">RepeatA입니다.</span><span class="sxs-lookup"><span data-stu-id="a08a4-121">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="a08a4-122">Microsoft 양자.</span><span class="sxs-lookup"><span data-stu-id="a08a4-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)