---
uid: Microsoft.Quantum.Diagnostics.FormattedFailure
title: FormattedFailure 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: FormattedFailure
qsharp.summary: Internal function used to fail with meaningful error messages.
ms.openlocfilehash: 6b1202c8897d67e3089a88a0855c8008b3a8c2ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98828271"
---
# <a name="formattedfailure-function"></a><span data-ttu-id="61031-102">FormattedFailure 함수</span><span class="sxs-lookup"><span data-stu-id="61031-102">FormattedFailure function</span></span>

<span data-ttu-id="61031-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="61031-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="61031-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="61031-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="61031-105">의미 있는 오류 메시지와 함께 실패 하는 데 사용 되는 내부 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="61031-105">Internal function used to fail with meaningful error messages.</span></span>

```qsharp
function FormattedFailure<'T> (actual : 'T, expected : 'T, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="61031-106">입력</span><span class="sxs-lookup"><span data-stu-id="61031-106">Input</span></span>

### <a name="actual--t"></a><span data-ttu-id="61031-107">실제: ' t</span><span class="sxs-lookup"><span data-stu-id="61031-107">actual : 'T</span></span>




### <a name="expected--t"></a><span data-ttu-id="61031-108">예상: ' '</span><span class="sxs-lookup"><span data-stu-id="61031-108">expected : 'T</span></span>




### <a name="message--string"></a><span data-ttu-id="61031-109">메시지: [문자열](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="61031-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>





## <a name="output--unit"></a><span data-ttu-id="61031-110">출력: [단위](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="61031-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="61031-111">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="61031-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="61031-112">없습니다</span><span class="sxs-lookup"><span data-stu-id="61031-112">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="61031-113">설명</span><span class="sxs-lookup"><span data-stu-id="61031-113">Remarks</span></span>

<span data-ttu-id="61031-114">이 함수는 전달 형식이 지정 된 모순를 허용 하기 위해 시뮬레이션 런타임에 의해 에뮬레이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61031-114">This function is intended to be emulated by simulation runtimes, so as to allow forwarding formatted contradictions.</span></span>