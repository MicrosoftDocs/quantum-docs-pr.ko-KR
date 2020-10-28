---
uid: Microsoft.Quantum.Diagnostics.EnableTestingViaName
title: EnableTestingViaName 사용자 정의 형식
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: EnableTestingViaName
qsharp.summary: Compiler-recognized attribute via which an alternative name can be defined that may be used when loading a type or callable for testing purposes.
ms.openlocfilehash: ee4f32a5af4243ad85994c2edd006737a5131931
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712846"
---
# <a name="enabletestingvianame-user-defined-type"></a><span data-ttu-id="04b8a-102">EnableTestingViaName 사용자 정의 형식</span><span class="sxs-lookup"><span data-stu-id="04b8a-102">EnableTestingViaName user defined type</span></span>

<span data-ttu-id="04b8a-103">네임 스페이스: [Microsoft. 양자 진단](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="04b8a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="04b8a-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="04b8a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="04b8a-105">컴파일러에서 인식할 수 있는 특성으로, 형식을 로드 하거나 테스트 목적으로 호출할 때 사용할 수 있는 대체 이름을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04b8a-105">Compiler-recognized attribute via which an alternative name can be defined that may be used when loading a type or callable for testing purposes.</span></span>

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype EnableTestingViaName = (String);
```

