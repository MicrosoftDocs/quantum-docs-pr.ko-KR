---
uid: Microsoft.Quantum.Synthesis.MCMTMask
title: MCMTMask 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: MCMTMask
qsharp.summary: >-
  A type to represent a multiple-controlled multiple-target Toffoli gate.

  The first integer is a bit mask for control lines.  Bit indexes which are set correspond to control line indexes.

  The second integer is a bit mask for target lines.  Bit indexes which are set correspond to target line indexes.

  The bit indexes of both integers must be disjoint.
ms.openlocfilehash: 0d3ca12d55fa4b5e8332d50939954de29e39b715
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725499"
---
# <a name="mcmtmask-user-defined-type"></a><span data-ttu-id="5bbd4-102">MCMTMask 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="5bbd4-102">MCMTMask user defined type</span></span>

<span data-ttu-id="5bbd4-103">네임 스페이스: [Microsoft 양자](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="5bbd4-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="5bbd4-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5bbd4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5bbd4-105">다중 제어 되는 여러 대상 Toffoli gate를 나타내는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-105">A type to represent a multiple-controlled multiple-target Toffoli gate.</span></span>

<span data-ttu-id="5bbd4-106">첫 번째 정수는 컨트롤 줄의 비트 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-106">The first integer is a bit mask for control lines.</span></span>  <span data-ttu-id="5bbd4-107">설정 되는 비트 인덱스는 줄 인덱스 제어에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-107">Bit indexes which are set correspond to control line indexes.</span></span>

<span data-ttu-id="5bbd4-108">두 번째 정수는 대상 줄의 비트 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-108">The second integer is a bit mask for target lines.</span></span>  <span data-ttu-id="5bbd4-109">설정 되는 비트 인덱스는 대상 줄 인덱스에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-109">Bit indexes which are set correspond to target line indexes.</span></span>

<span data-ttu-id="5bbd4-110">두 정수의 비트 인덱스는 분리 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-110">The bit indexes of both integers must be disjoint.</span></span>

```qsharp

newtype MCMTMask = (ControlMask : Int, TargetMask : Int);
```



## <a name="named-items"></a><span data-ttu-id="5bbd4-111">명명 된 항목</span><span class="sxs-lookup"><span data-stu-id="5bbd4-111">Named Items</span></span>

### <a name="controlmask--int"></a><span data-ttu-id="5bbd4-112">ControlMask: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5bbd4-112">ControlMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="targetmask--int"></a><span data-ttu-id="5bbd4-113">TargetMask: [Int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5bbd4-113">TargetMask : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

