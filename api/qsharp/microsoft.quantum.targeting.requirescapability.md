---
uid: Microsoft.Quantum.Targeting.RequiresCapability
title: RequiresCapability 사용자 정의 형식
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Targeting
qsharp.name: RequiresCapability
qsharp.summary: Compiler-recognized attribute used to mark a callable with the runtime capabilities it requires.
ms.openlocfilehash: 5e0db49d6f73398ac36003eb0f44e3a6520b7f1e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855147"
---
# <a name="requirescapability-user-defined-type"></a>RequiresCapability 사용자 정의 형식

네임 스페이스: [Microsoft 양자. 대상](xref:Microsoft.Quantum.Targeting)

패키지: [Microsoft. 양자](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


필요한 런타임 기능으로 호출할 수 있는를 표시 하는 데 사용 되는 컴파일러 인식 특성입니다.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype RequiresCapability = (Level : String, Reason : String);
```



## <a name="named-items"></a>명명 된 항목

### <a name="level--string"></a>수준: [문자열](xref:microsoft.quantum.lang-ref.string)

호출 가능에서 요구 하는 런타임 기능 수준의 이름입니다.
### <a name="reason--string"></a>이유: [문자열](xref:microsoft.quantum.lang-ref.string)

호출에이 런타임 기능이 필요한 이유에 대 한 설명입니다.

## <a name="remarks"></a>설명

이 특성의 인스턴스가 호출 가능에 이미 존재 하지 않는 경우이 특성은 컴파일러의 callables에 자동으로 추가 됩니다. 컴파일러에서 필요한 기능을 올바르게 유추 하지 않는 드문 경우를 제외 하 고는 사용 하지 않아야 합니다.

다음은 기능 수준 이름 목록으로, 용량을 늘리거나 제한 합니다.

## `"BasicQuantumFunctionality"`

측정 결과와 같음 비교를 비교할 수 없습니다.

## `"BasicMeasurementFeedback"`

연산에서 if 문 조건 식의 같음에 대해서만 측정 결과를 비교할 수 있습니다. 결과에 따라 달라 지는 문의 블록은 블록 외부에 선언 된 변경 가능한 변수 또는 return 문으로 set 문을 포함할 수 없습니다.

## `"FullComputation"`

런타임 제한이 없습니다. 모든 Q # 프로그램을 실행할 수 있습니다.