---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: PrepareIdentity 작업
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: a3f96fbdafb19c90fb2b563243600cca60841566
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724890"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="421e3-102">PrepareIdentity 작업</span><span class="sxs-lookup"><span data-stu-id="421e3-102">PrepareIdentity operation</span></span>

<span data-ttu-id="421e3-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="421e3-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="421e3-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="421e3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="421e3-105">레지스터가 지정 된 경우 최대 혼합 상태에서 등록을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="421e3-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="421e3-106">레지스터는 각 \boldone에 전체 depolarizing 채널을 적용 하 여 $/2 ^ N $ 상태에서 준비 됩니다. 여기서 $N $은 레지스터의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="421e3-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="421e3-107">입력</span><span class="sxs-lookup"><span data-stu-id="421e3-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="421e3-108">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="421e3-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="421e3-109">위에서 설명한 방식으로 해당 상태가 depolarized 인 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="421e3-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="421e3-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="421e3-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="421e3-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="421e3-111">See Also</span></span>

- [<span data-ttu-id="421e3-112">PrepareSingleQubitIdentity.</span><span class="sxs-lookup"><span data-stu-id="421e3-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)