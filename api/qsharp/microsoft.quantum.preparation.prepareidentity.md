---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: PrepareIdentity 작업
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: ec7e813110ccd9e6d499fc469fa27249a182b870
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855882"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="0f67b-102">PrepareIdentity 작업</span><span class="sxs-lookup"><span data-stu-id="0f67b-102">PrepareIdentity operation</span></span>

<span data-ttu-id="0f67b-103">네임 스페이스: [Microsoft 양자 준비](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="0f67b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="0f67b-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0f67b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0f67b-105">레지스터가 지정 된 경우 최대 혼합 상태에서 등록을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f67b-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="0f67b-106">레지스터는 각 \boldone에 전체 depolarizing 채널을 적용 하 여 $/2 ^ N $ 상태에서 준비 됩니다. 여기서 $N $은 레지스터의 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="0f67b-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0f67b-107">입력</span><span class="sxs-lookup"><span data-stu-id="0f67b-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="0f67b-108">register: [](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0f67b-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0f67b-109">위에서 설명한 방식으로 해당 상태가 depolarized 인 레지스터입니다.</span><span class="sxs-lookup"><span data-stu-id="0f67b-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0f67b-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0f67b-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0f67b-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0f67b-111">See Also</span></span>

- [<span data-ttu-id="0f67b-112">PrepareSingleQubitIdentity.</span><span class="sxs-lookup"><span data-stu-id="0f67b-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)