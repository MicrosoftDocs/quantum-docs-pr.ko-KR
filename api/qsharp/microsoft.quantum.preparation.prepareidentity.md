---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: PrepareIdentity 작업
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: 6e0a43e61e3c49edef94db63f07ed29132d84c83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210440"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="39c9a-102">PrepareIdentity 작업</span><span class="sxs-lookup"><span data-stu-id="39c9a-102">PrepareIdentity operation</span></span>

<span data-ttu-id="39c9a-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="39c9a-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="39c9a-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39c9a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39c9a-105">레지스터가 지정 된 경우 최대 혼합 상태에서 등록을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="39c9a-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="39c9a-106">레지스터는 각 \boldone에 전체 depolarizing 채널을 적용 하 여 $/2 ^ N $ 상태에서 준비 됩니다. 여기서 $N $은 레지스터의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="39c9a-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="39c9a-107">입력</span><span class="sxs-lookup"><span data-stu-id="39c9a-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="39c9a-108">register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="39c9a-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="39c9a-109">위에서 설명한 방식으로 해당 상태가 depolarized 인 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="39c9a-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39c9a-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39c9a-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="39c9a-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="39c9a-111">See Also</span></span>

- [<span data-ttu-id="39c9a-112">PrepareSingleQubitIdentity.</span><span class="sxs-lookup"><span data-stu-id="39c9a-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)