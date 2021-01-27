---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: GreaterThan 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 553efb0fc83f24235cb4a77933bd1d547bbd1fed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846626"
---
# <a name="greaterthan-operation"></a><span data-ttu-id="3900d-102">GreaterThan 작업</span><span class="sxs-lookup"><span data-stu-id="3900d-102">GreaterThan operation</span></span>

<span data-ttu-id="3900d-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3900d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3900d-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3900d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3900d-105">비교 결과에 따라 대상의 범위를 대칭 이동 하는 두 개의 정수를 해당 형식으로 인코딩된 두 정수 사이에 보다 큼 비교를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3900d-105">Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.</span></span>

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="3900d-106">설명</span><span class="sxs-lookup"><span data-stu-id="3900d-106">Description</span></span>

<span data-ttu-id="3900d-107">$ 및 $y $ $x 두 정수의 비교를 엄격 하 게 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="3900d-107">Carries out a strictly greater than comparison of two integers $x$ and $y$, encoded in qubit registers xs and ys.</span></span> <span data-ttu-id="3900d-108">Y $를 > $x 경우에는 결과의 비트가 대칭 이동 됩니다. 그렇지 않으면 결과의 비트가 상태를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3900d-108">If $x > y$, then the result qubit will be flipped, otherwise the result qubit will retain its state.</span></span>

## <a name="input"></a><span data-ttu-id="3900d-109">입력</span><span class="sxs-lookup"><span data-stu-id="3900d-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="3900d-110">xs: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3900d-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3900d-111">LittleEndian vebit는 첫 번째 정수 $x $로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="3900d-111">LittleEndian qubit register encoding the first integer $x$.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="3900d-112">작업: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3900d-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3900d-113">LittleEndian cobit $y $의 두 번째 정수를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3900d-113">LittleEndian qubit register encoding the second integer $y$.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="3900d-114">결과: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3900d-114">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3900d-115">$X > y $ 인 경우 대칭 이동 될 단일 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="3900d-115">Single qubit that will be flipped if $x > y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3900d-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3900d-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3900d-117">설명</span><span class="sxs-lookup"><span data-stu-id="3900d-117">Remarks</span></span>

<span data-ttu-id="3900d-118">는 $x-y = (x ' + y) ' $를 사용 합니다. 여기서은 1의 보수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3900d-118">Uses the trick that $x - y = (x'+y)'$, where ' denotes the one's complement.</span></span>

## <a name="references"></a><span data-ttu-id="3900d-119">참조</span><span class="sxs-lookup"><span data-stu-id="3900d-119">References</span></span>

- <span data-ttu-id="3900d-120">Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new 퀀텀 ripple and A new, 2004.</span><span class="sxs-lookup"><span data-stu-id="3900d-120">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1

- <span data-ttu-id="3900d-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "2n를 사용 하는 Toffoli + 2 based 모듈형 곱셈", 2016 https://arxiv.org/abs/1611.07995</span><span class="sxs-lookup"><span data-stu-id="3900d-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "Factoring using 2n+2 qubits with Toffoli based modular multiplication", 2016 https://arxiv.org/abs/1611.07995</span></span>