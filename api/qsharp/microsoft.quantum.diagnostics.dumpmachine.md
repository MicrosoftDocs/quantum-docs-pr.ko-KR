---
uid: Microsoft.Quantum.Diagnostics.DumpMachine
title: 로 컴퓨터 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpMachine
qsharp.summary: Dumps the current target machine's status.
ms.openlocfilehash: c85cf6764bdc913a71448c525318f45743bf1df0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712874"
---
# <a name="dumpmachine-function"></a><span data-ttu-id="6fe15-102">로 컴퓨터 함수</span><span class="sxs-lookup"><span data-stu-id="6fe15-102">DumpMachine function</span></span>

<span data-ttu-id="6fe15-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="6fe15-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="6fe15-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6fe15-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6fe15-105">현재 대상 컴퓨터의 상태를 덤프 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe15-105">Dumps the current target machine's status.</span></span>

```qsharp
function DumpMachine<'T> (location : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="6fe15-106">입력</span><span class="sxs-lookup"><span data-stu-id="6fe15-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="6fe15-107">위치: ' '</span><span class="sxs-lookup"><span data-stu-id="6fe15-107">location : 'T</span></span>

<span data-ttu-id="6fe15-108">컴퓨터의 덤프를 생성 하는 위치에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe15-108">Provides information on where to generate the machine's dump.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6fe15-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6fe15-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="6fe15-110">없음</span><span class="sxs-lookup"><span data-stu-id="6fe15-110">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6fe15-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6fe15-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6fe15-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="6fe15-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="6fe15-113">설명</span><span class="sxs-lookup"><span data-stu-id="6fe15-113">Remarks</span></span>

<span data-ttu-id="6fe15-114">이 메서드를 사용 하면 대상 컴퓨터의 현재 상태에 대 한 정보를 파일 또는 다른 위치에 덤프할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fe15-114">This method allows you to dump information about the current status of the target machine into a file or some other location.</span></span>
<span data-ttu-id="6fe15-115">의 실제 정보 및 의미 체계는 `location` 각 대상 컴퓨터에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fe15-115">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="6fe15-116">그러나 빈 튜플을 위치 ()로 제공 `()` 하거나 매개 변수를 생략 하는 것은 `location` 일반적으로 콘솔에 대 한 출력을 생성 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fe15-116">However, providing an empty tuple as a location (`()`) or just omitting the `location` parameter typically means to generate the output to the console.</span></span>

<span data-ttu-id="6fe15-117">퀀텀 개발 키트의 일부로 분산 된 로컬 전체 상태 시뮬레이터의 경우이 메서드는 웨이브 함수를 복소수의 1 차원 배열로 기록 하는 파일에 대 한 경로가 포함 된 문자열을 예상 합니다. 여기서 각 요소는 해당 상태를 측정할 확률의 amplitudes을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6fe15-117">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the wave function as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>