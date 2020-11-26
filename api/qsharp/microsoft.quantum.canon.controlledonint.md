---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: ControlledOnInt 함수
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3cc5c00d9c7295106901149e06571ef1963d1323
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207261"
---
# <a name="controlledonint-function"></a><span data-ttu-id="cff23-102">ControlledOnInt 함수</span><span class="sxs-lookup"><span data-stu-id="cff23-102">ControlledOnInt function</span></span>

<span data-ttu-id="cff23-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cff23-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cff23-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cff23-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cff23-105">컨트롤 레지스터 상태가 지정 된 양의 정수에 해당 하는 경우 대상 레지스터에 oracle을 적용 하는 단일 연산자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff23-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="cff23-106">입력</span><span class="sxs-lookup"><span data-stu-id="cff23-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="cff23-107">번호 상태: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cff23-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cff23-108">양의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="cff23-108">Positive integer.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="cff23-109">oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="cff23-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="cff23-110">단일 연산자.</span><span class="sxs-lookup"><span data-stu-id="cff23-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="cff23-111">출력[: (Adj](xref:microsoft.quantum.lang-ref.qubit)+ [], ' t) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl + Ctl</span><span class="sxs-lookup"><span data-stu-id="cff23-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="cff23-112">`oracle`컨트롤 레지스터 상태가 숫자 상태에 해당 하는 경우 대상 레지스터에 적용 되는 단일 연산자입니다 `numberState` .</span><span class="sxs-lookup"><span data-stu-id="cff23-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cff23-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cff23-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cff23-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="cff23-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="cff23-115">설명</span><span class="sxs-lookup"><span data-stu-id="cff23-115">Remarks</span></span>

<span data-ttu-id="cff23-116">의 값은 `numberState` 작은 endian 인코딩을 사용 하 여 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cff23-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>