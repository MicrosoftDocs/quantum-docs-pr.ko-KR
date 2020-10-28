---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: FormattedFailure 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 0d7fb01ddf23cd6d79f722c8f6b691afa74a8885
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712678"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="027cd-102">FormattedFailure 함수</span><span class="sxs-lookup"><span data-stu-id="027cd-102">FormattedFailure function</span></span>

<span data-ttu-id="027cd-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="027cd-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="027cd-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="027cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="027cd-105">의미 있는 오류 메시지와 함께 실패 하는 데 사용 되는 내부 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="027cd-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="027cd-106">입력</span><span class="sxs-lookup"><span data-stu-id="027cd-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="027cd-107">실제: ' t</span><span class="sxs-lookup"><span data-stu-id="027cd-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="027cd-108">예상: ' '</span><span class="sxs-lookup"><span data-stu-id="027cd-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="027cd-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="027cd-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="027cd-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="027cd-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="027cd-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="027cd-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="027cd-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="027cd-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="027cd-113">설명</span><span class="sxs-lookup"><span data-stu-id="027cd-113">Remarks</span></span>

<span data-ttu-id="027cd-114">이 함수는 전달 형식이 지정 된 모순를 허용 하기 위해 시뮬레이션 런타임에 의해 에뮬레이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="027cd-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>