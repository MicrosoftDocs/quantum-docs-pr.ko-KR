---
uid: Microsoft.Quantum.Intrinsic.Message
title: Message 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 652e33de69ffb725f117db3beeffa66558776f49
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849371"
---
# <a name="message-function"></a><span data-ttu-id="47626-102">Message 함수</span><span class="sxs-lookup"><span data-stu-id="47626-102">Message function</span></span>

<span data-ttu-id="47626-103">네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="47626-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="47626-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="47626-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="47626-105">메시지를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="47626-105">Logs a message.</span></span>

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="47626-106">입력</span><span class="sxs-lookup"><span data-stu-id="47626-106">Input</span></span>

### <a name="msg--string"></a><span data-ttu-id="47626-107">msg: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="47626-107">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="47626-108">보고할 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="47626-108">The message to be reported.</span></span>



## <a name="output--unit"></a><span data-ttu-id="47626-109">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="47626-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="47626-110">설명</span><span class="sxs-lookup"><span data-stu-id="47626-110">Remarks</span></span>

<span data-ttu-id="47626-111">이 함수의 특정 동작은 시뮬레이터에 종속 되지만 대부분의 경우 지정 된 메시지가 콘솔에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47626-111">The specific behavior of this function is simulator-dependent, but in most cases the given message will be written to the console.</span></span>