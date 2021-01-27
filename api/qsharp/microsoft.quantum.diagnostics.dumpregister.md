---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: DumpRegister 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: 835c7a9edb22b4be630ebfc04587c12b3ff668b2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829226"
---
# <a name="dumpregister-function"></a><span data-ttu-id="f8a85-102">DumpRegister 함수</span><span class="sxs-lookup"><span data-stu-id="f8a85-102">DumpRegister function</span></span>

<span data-ttu-id="f8a85-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f8a85-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f8a85-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f8a85-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f8a85-105">지정 된 비트와 연결 된 현재 대상 컴퓨터의 상태를 덤프 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-105">Dumps the current target machine's status associated with the given qubits.</span></span>

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f8a85-106">입력</span><span class="sxs-lookup"><span data-stu-id="f8a85-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="f8a85-107">위치: ' '</span><span class="sxs-lookup"><span data-stu-id="f8a85-107">location : 'T</span></span>

<span data-ttu-id="f8a85-108">상태 덤프를 생성할 위치에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-108">Provides information on where to generate the state's dump.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="f8a85-109">작업 비트: 고 [비트](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f8a85-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f8a85-110">보고할 비트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-110">The list of qubits to report.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f8a85-111">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f8a85-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="f8a85-112">없음</span><span class="sxs-lookup"><span data-stu-id="f8a85-112">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f8a85-113">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8a85-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f8a85-114">없습니다</span><span class="sxs-lookup"><span data-stu-id="f8a85-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="f8a85-115">설명</span><span class="sxs-lookup"><span data-stu-id="f8a85-115">Remarks</span></span>

<span data-ttu-id="f8a85-116">이 메서드를 사용 하면 지정 된 비트의 상태와 연결 된 정보를 파일 또는 다른 위치에 덤프할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-116">This method allows you to dump the information associated with the state of the given qubits into a file or some other location.</span></span>
<span data-ttu-id="f8a85-117">의 실제 정보 및 의미 체계는 `location` 각 대상 컴퓨터에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-117">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="f8a85-118">그러나 빈 튜플을 위치 ()로 제공 하면 `()` 일반적으로 콘솔에 대 한 출력을 생성 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-118">However, providing an empty tuple as a location (`()`) typically means to generate the output to the console.</span></span>

<span data-ttu-id="f8a85-119">퀀텀 개발 키트의 일부로 분산 된 로컬 전체 상태 시뮬레이터의 경우이 메서드는 지정 된 요소 (즉, 해당 하위 시스템의 wave 함수)의 상태를 해당 상태를 측정할 확률의 amplitudes을 나타내는 복소수의 1 차원 배열로 기록 하는 파일에 대 한 경로가 포함 된 문자열을 예상 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-119">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the state of the given qubits (i.e. the wave function of the corresponding  subsystem) as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>
<span data-ttu-id="f8a85-120">지정 된 비트를 다른 몇 가지 다른 것으로 지정 하 고 해당 상태를 분리할 수 없는 경우,이는 해당 하는 것을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8a85-120">If the given qubits are entangled with some other qubit and their state can't be separated, it just reports that the qubits are entangled.</span></span>