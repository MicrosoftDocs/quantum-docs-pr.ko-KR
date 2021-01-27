---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: InjectPi4YRotation 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 249c347c9e9729e719eda69e4e9a21847d9a46eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825954"
---
# <a name="injectpi4yrotation-operation"></a><span data-ttu-id="503aa-102">InjectPi4YRotation 작업</span><span class="sxs-lookup"><span data-stu-id="503aa-102">InjectPi4YRotation operation</span></span>

<span data-ttu-id="503aa-103">네임 스페이스: [Microsoft 양자 수정](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="503aa-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="503aa-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="503aa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="503aa-105">Y 축에 대해 π/4를 기준으로 단일의 비트를 회전 합니다.</span><span class="sxs-lookup"><span data-stu-id="503aa-105">Rotates a single qubit by π/4 about the Y-axis.</span></span>

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="503aa-106">설명</span><span class="sxs-lookup"><span data-stu-id="503aa-106">Description</span></span>

<span data-ttu-id="503aa-107">에 대해 π/4 회전을 수행 `Y` 합니다.</span><span class="sxs-lookup"><span data-stu-id="503aa-107">Performs a π/4 rotation about `Y`.</span></span>

<span data-ttu-id="503aa-108">회전은 매직 상태를 사용 하 여 수행 됩니다. 즉, $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} \ket 상태를 복사 합니다 {8} {1} .</span><span class="sxs-lookup"><span data-stu-id="503aa-108">The rotation is performed by consuming a magic state; that is, a copy of the state $$ \begin{align} \cos\frac{\pi}{8} \ket{0} + \sin \frac{\pi}{8} \ket{1}.</span></span>
<span data-ttu-id="503aa-109">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="503aa-109">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="503aa-110">입력</span><span class="sxs-lookup"><span data-stu-id="503aa-110">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="503aa-111">데이터: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="503aa-111">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="503aa-112">$ \Pi/$4에 대 한 $Y $에 대해 회전 하는 데 사용할 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="503aa-112">A qubit to be rotated about $Y$ by $\pi / 4$.</span></span>


### <a name="magic--qubit"></a><span data-ttu-id="503aa-113">마법: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="503aa-113">magic : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="503aa-114">초기 상태의 초기 상태에 있는 놀라운 비트입니다.</span><span class="sxs-lookup"><span data-stu-id="503aa-114">A qubit initially in the magic state.</span></span> <span data-ttu-id="503aa-115">이 작업의 다음 응용 프로그램이 `magic` $ \ket $ 상태로 반환 됩니다 {0} .</span><span class="sxs-lookup"><span data-stu-id="503aa-115">Following application of this operation, `magic` is returned to the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="503aa-116">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="503aa-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="503aa-117">설명</span><span class="sxs-lookup"><span data-stu-id="503aa-117">Remarks</span></span>

<span data-ttu-id="503aa-118">다음은 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="503aa-118">The following are equivalent:</span></span>

```qsharp
Ry(PI() / 4.0, data);
```

<span data-ttu-id="503aa-119">및</span><span class="sxs-lookup"><span data-stu-id="503aa-119">and</span></span>

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

<span data-ttu-id="503aa-120">이 작업은 동작을 지원 합니다 .이 `Adjoint` 경우 동일한 매직 상태를 사용 하지만 데이터의 효과는 $-\ pi/4 $ $Y $-회전입니다.</span><span class="sxs-lookup"><span data-stu-id="503aa-120">This operation supports the `Adjoint` functor, in which case the same magic state is consumed, but the effect on the data qubit is a $-\pi/4$ $Y$-rotation.</span></span>