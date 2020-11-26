---
uid: Microsoft.Quantum.Core.EntryPoint
title: EntryPoint 사용자 정의 형식
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: EntryPoint
qsharp.summary: Compiler-recognized attribute used to mark the entry point of an executable.
ms.openlocfilehash: 671b363e8b87fff0774bc42222cb57062f2a99c8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213908"
---
# <a name="entrypoint-user-defined-type"></a>EntryPoint 사용자 정의 형식

네임 스페이스: [Microsoft. 양자](xref:Microsoft.Quantum.Core)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


실행 파일의 진입점을 표시 하는 데 사용 되는 컴파일러 인식 특성입니다.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype EntryPoint = (Unit);
```

