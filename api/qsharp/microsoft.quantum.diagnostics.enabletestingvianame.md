---
uid: Microsoft.Quantum.Diagnostics.EnableTestingViaName
title: EnableTestingViaName 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EnableTestingViaName
qsharp.summary: Compiler-recognized attribute via which an alternative name can be defined that may be used when loading a type or callable for testing purposes.
ms.openlocfilehash: c488b6f3d22fd0c6d4e950070464e914f757654c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853388"
---
# <a name="enabletestingvianame-user-defined-type"></a><span data-ttu-id="2af48-102">EnableTestingViaName 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="2af48-102">EnableTestingViaName user defined type</span></span>

<span data-ttu-id="2af48-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="2af48-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="2af48-104">패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2af48-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2af48-105">컴파일러에서 인식할 수 있는 특성으로, 형식을 로드 하거나 테스트 목적으로 호출할 때 사용할 수 있는 대체 이름을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2af48-105">Compiler-recognized attribute via which an alternative name can be defined that may be used when loading a type or callable for testing purposes.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype EnableTestingViaName = (String);
```

