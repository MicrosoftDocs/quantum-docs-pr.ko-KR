---
uid: Microsoft.Quantum.Intrinsic.Message
title: Message 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 0428a46bc639bc8a0697f5bd392f85b8b9f40ee5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711425"
---
# <a name="message-function"></a><span data-ttu-id="c453b-102">Message 함수</span><span class="sxs-lookup"><span data-stu-id="c453b-102">Message function</span></span>

<span data-ttu-id="c453b-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c453b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c453b-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c453b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c453b-105">메시지를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c453b-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="c453b-106">입력</span><span class="sxs-lookup"><span data-stu-id="c453b-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="c453b-107">msg: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c453b-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c453b-108">보고할 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="c453b-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c453b-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c453b-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c453b-110">설명</span><span class="sxs-lookup"><span data-stu-id="c453b-110">Remarks</span></span>

<span data-ttu-id="c453b-111">이 함수의 특정 동작은 시뮬레이터에 종속 되지만 대부분의 경우 지정 된 메시지가 콘솔에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c453b-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>