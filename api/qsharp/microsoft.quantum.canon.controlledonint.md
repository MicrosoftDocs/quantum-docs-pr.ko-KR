---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: ControlledOnInt 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716416"
---
# <a name="controlledonint-function"></a><span data-ttu-id="0cca9-102">ControlledOnInt 함수</span><span class="sxs-lookup"><span data-stu-id="0cca9-102">ControlledOnInt function</span></span>

<span data-ttu-id="0cca9-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0cca9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0cca9-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0cca9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0cca9-105">컨트롤 레지스터 상태가 지정 된 양의 정수에 해당 하는 경우 대상 레지스터에 oracle을 적용 하는 단일 연산자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cca9-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="0cca9-106">입력</span><span class="sxs-lookup"><span data-stu-id="0cca9-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="0cca9-107">번호 상태: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0cca9-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0cca9-108">양의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="0cca9-108">Positive integer.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="0cca9-109">oracle: ' t => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="0cca9-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="0cca9-110">단일 연산자.</span><span class="sxs-lookup"><span data-stu-id="0cca9-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="0cca9-111">출력: ([Adj []](xref:microsoft.quantum.lang-ref.qubit), ' t) => [Unit](xref:microsoft.quantum.lang-ref.unit) + Ctl</span><span class="sxs-lookup"><span data-stu-id="0cca9-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="0cca9-112">`oracle`컨트롤 레지스터 상태가 숫자 상태에 해당 하는 경우 대상 레지스터에 적용 되는 단일 연산자입니다 `numberState` .</span><span class="sxs-lookup"><span data-stu-id="0cca9-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0cca9-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0cca9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0cca9-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="0cca9-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="0cca9-115">설명</span><span class="sxs-lookup"><span data-stu-id="0cca9-115">Remarks</span></span>

<span data-ttu-id="0cca9-116">의 값은 `numberState` 작은 endian 인코딩을 사용 하 여 해석 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cca9-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>