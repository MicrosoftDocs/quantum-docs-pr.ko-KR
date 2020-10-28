---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: RequiresCapability 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 63b1952d402f1bcb81a8f9d0afc3cdf7aa7e5ed8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725135"
---
# <a name="requirescapability-user-defined-type"></a><span data-ttu-id="95411-102">RequiresCapability 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="95411-102">RequiresCapability user defined type</span></span>

<span data-ttu-id="95411-103">네임 스페이스: [Microsoft 양자. 대상](xref:Microsoft.Quantum.Targeting)</span><span class="sxs-lookup"><span data-stu-id="95411-103">Namespace: [Microsoft.Quantum.Targeting](xref:Microsoft.Quantum.Targeting)</span></span>

<span data-ttu-id="95411-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="95411-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="95411-105">필요한 런타임 기능으로 호출할 수 있는를 표시 하는 데 사용 되는 컴파일러 인식 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="95411-105">Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a><span data-ttu-id="95411-106">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="95411-106">Named Items</span></span>

### <a name="level--string"></a><span data-ttu-id="95411-107">수준: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="95411-107">Level : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="95411-108">호출 가능에서 요구 하는 런타임 기능 수준의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95411-108">The name of the runtime capability level required by the callable.</span></span>
### <a name="reason--string"></a><span data-ttu-id="95411-109">이유: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="95411-109">Reason : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="95411-110">호출에이 런타임 기능이 필요한 이유에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="95411-110">A description of why the callable requires this runtime capability.</span></span>

## <a name="remarks"></a><span data-ttu-id="95411-111">설명</span><span class="sxs-lookup"><span data-stu-id="95411-111">Remarks</span></span>

<span data-ttu-id="95411-112">이 특성의 인스턴스가 호출 가능에 이미 존재 하지 않는 경우이 특성은 컴파일러의 callables에 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95411-112">This attribute is automatically added to callables by the compiler, unless an instance of this attribute already exists on the callable.</span></span> <span data-ttu-id="95411-113">컴파일러에서 필요한 기능을 올바르게 유추 하지 않는 드문 경우를 제외 하 고는 사용 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95411-113">It should not be used except in rare cases where the compiler does not infer the required capability correctly.</span></span>

<span data-ttu-id="95411-114">다음은 기능 수준 이름 목록으로, 용량을 늘리거나 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="95411-114">Below is the list of capability level names, in order of increasing capabilities or decreasing restrictions:</span></span>

## `"BasicQuantumFunctionality"`

<span data-ttu-id="95411-115">측정 결과와 같음 비교를 비교할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95411-115">Measurement results cannot be compared for equality.</span></span>

## `"BasicMeasurementFeedback"`

<span data-ttu-id="95411-116">연산에서 if 문 조건 식의 같음에 대해서만 측정 결과를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95411-116">Measurement results can be compared for equality only in if-statement conditional expressions in operations.</span></span> <span data-ttu-id="95411-117">결과에 따라 달라 지는 문의 블록은 블록 외부에 선언 된 변경 가능한 변수 또는 return 문으로 set 문을 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95411-117">The block of an if-statement that depends on a result cannot contain set statements for mutable variables declared outside the block, or return statements.</span></span>

## `"FullComputation"`

<span data-ttu-id="95411-118">런타임 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95411-118">No runtime restrictions.</span></span> <span data-ttu-id="95411-119">모든 Q # 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95411-119">Any Q# program can be executed.</span></span>