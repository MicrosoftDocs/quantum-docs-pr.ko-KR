---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: ApplyToRestCA 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: e64eeaae2151a28c289e3e71e47f897d6c378b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841254"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="f9dcc-102">ApplyToRestCA 작업</span><span class="sxs-lookup"><span data-stu-id="f9dcc-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="f9dcc-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f9dcc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f9dcc-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f9dcc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f9dcc-105">배열의 첫 번째 요소를 제외한 모든 요소에 작업을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9dcc-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="f9dcc-106">설명</span><span class="sxs-lookup"><span data-stu-id="f9dcc-106">Description</span></span>

<span data-ttu-id="f9dcc-107">작업 `op` 및 대상 배열이 지정 된 `targets` 경우가 적용 됩니다 `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="f9dcc-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="f9dcc-108">입력</span><span class="sxs-lookup"><span data-stu-id="f9dcc-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="f9dcc-109">op: ' t [] => [Unit](xref:microsoft.quantum.lang-ref.unit)  이 Adj + Ctl입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dcc-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="f9dcc-110">적용 될 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dcc-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="f9dcc-111">대상: ' t []</span><span class="sxs-lookup"><span data-stu-id="f9dcc-111">targets : 'T[]</span></span>

<span data-ttu-id="f9dcc-112">첫 번째가 적용 되는 대상의 배열입니다 `op` .</span><span class="sxs-lookup"><span data-stu-id="f9dcc-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f9dcc-113">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9dcc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f9dcc-114">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9dcc-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f9dcc-115">없습니다</span><span class="sxs-lookup"><span data-stu-id="f9dcc-115">'T</span></span>

<span data-ttu-id="f9dcc-116">적용할 작업의 입력 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dcc-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9dcc-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f9dcc-117">See Also</span></span>

- [<span data-ttu-id="f9dcc-118">Microsoft. 양자. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="f9dcc-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="f9dcc-119">Microsoft. 양자. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="f9dcc-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="f9dcc-120">Microsoft. 양자. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="f9dcc-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)