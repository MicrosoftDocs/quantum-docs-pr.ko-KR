---
title: 양자 시뮬레이터 및 클래식 드라이버 | Microsoft Docs
description: 클래식 컴퓨팅 .NET 언어(일반적으로 C# 또는 Q#)를 사용하여 양자 시뮬레이터을 구동하는 방법을 설명합니다.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 5ac79280669ae0acfe993a1c2ae1c069b0c01848
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035112"
---
# <a name="classical-drivers-and-machines"></a>클래식 드라이버 및 컴퓨터

## <a name="what-youll-learn"></a>학습할 내용

> [!div class="checklist"]
> * 양자 알고리즘을 실행하는 방법
> * 이 릴리스에 포함된 양자 시뮬레이터
> * 양자 알고리즘용 C# 드라이버를 작성하는 방법

## <a name="the-quantum-development-kit-execution-model"></a>Quantum Development Kit 실행 모델

[양자 프로그램을 작성](xref:microsoft.quantum.write-program)할 때 `QuantumSimulator` 개체를 알고리즘 클래스의 `Run` 메서드에 전달하여 양자 알고리즘을 실행했습니다.
`QuantumSimulator` 클래스는 `Teleport`를 실행하고 테스트하는 데 적합한 양자 상태 벡터를 완전히 시뮬레이션하여 양자 알고리즘을 실행합니다.
양자 상태 벡터에 대한 자세한 내용은 [개념 가이드](xref:microsoft.quantum.concepts.intro)를 참조하세요.

양자 알고리즘을 실행하는 데 다른 대상 컴퓨터를 사용할 수도 있습니다.
컴퓨터는 이 알고리즘을 위한 양자 기본 형식을 구현합니다.
여기에는 H, CNOT 및 측정과 같은 기본 작업 뿐만 아니라, 큐비트 관리와 추적도 포함됩니다.
여러 다른 클래스의 양자 컴퓨터는 동일한 양자 알고리즘에 대해 서로 다른 실행 모델을 나타냅니다.

각 유형의 양자 컴퓨터는 이러한 기본 형식의 다른 구현을 제공할 수 있습니다.
예를 들어, 개발 키트에 포함된 양자 컴퓨터 추적 시뮬레이터는 시뮬레이션을 전혀 수행하지 않습니다.
대신 알고리즘에 대한 게이트, 큐비트 및 기타 리소스 사용을 추적합니다.

### <a name="quantum-machines"></a>양자 컴퓨터

향후, 다른 유형의 시뮬레이션을 지원하고 토폴로지 양자 컴퓨터에서 실행할 수 있도록 지원하는 추가 양자 컴퓨터 클래스를 정의할 예정입니다.
기본 컴퓨터 구현을 변경하면서 알고리즘은 일정하게 유지하면 시뮬레이션에서 알고리즘을 쉽게 테스트하고 디버그한 다음, 알고리즘이 변경되지 않았다는 확신을 가지고 실제 하드웨어에서 실행할 수 있습니다.

### <a name="whats-included-in-this-release"></a>이 릴리스에 포함된 내용

이 버전의 양자 개발자 키트에는 몇 가지 양자 컴퓨터 클래스가 포함되어 있습니다.
이러한 모든 항목은 `Microsoft.Quantum.Simulation.Simulators` 네임스페이스에 정의됩니다.

* [전체 상태 벡터 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` 클래스
* [단순 리소스 추정기](xref:microsoft.quantum.machines.resources-estimator), `ResourcesEstimator` 클래스. 양자 알고리즘을 실행하는 데 필요한 리소스를 최상위 수준에서 분석할 수 있도록 합니다.
* [추적 기반 리소스 추정기](xref:microsoft.quantum.machines.qc-trace-simulator.intro), `QCTraceSimulator` 클래스. 알고리즘의 전체 호출 그래프에 대해 리소스 사용량을 자세히 분석할 수 있습니다.
* [Toffoli 시뮬레이터](xref:microsoft.quantum.machines.toffoli-simulator), `ToffoliSimulator` 클래스

## <a name="writing-a-classical-driver-program"></a>클래식 드라이버 프로그램 작성

[양자 프로그램을 작성](xref:microsoft.quantum.write-program)할 때 간단한 텔레포트 알고리즘용 C# 드라이버를 작성했습니다. C# 드라이버는 다음과 같은 4가지 주요 목적으로 사용됩니다.

* 대상 컴퓨터 생성
* 양자 알고리즘에 필요한 인수 계산
* 시뮬레이터를 사용하여 양자 알고리즘 실행
* 연산 결과 처리

여기서는 각 단계를 좀 더 자세히 설명합니다.

### <a name="constructing-the-target-machine"></a>대상 컴퓨터 생성

양자 컴퓨터는 일반적인 .NET 클래스의 인스턴스로, .NET 클래스와 마찬가지로 해당 생성자를 호출하여 생성됩니다.
`QuantumSimulator`를 비롯한 일부 시뮬레이터는 .NET <xref:System.IDisposable?displayProperty=nameWithType> 인터페이스를 구현하므로 C# `using` 문에 래핑해야 합니다.

### <a name="computing-arguments-for-the-algorithm"></a>알고리즘의 인수 계산

`Teleport` 예제에서는 몇 가지 상대적인 인공 인수를 계산하여 양자 알고리즘에 전달했습니다.
그러나 일반적으로 양자 알고리즘에는 많은 데이터가 필요하며, 클래식 드라이버에서 이러한 데이터를 제공하는 것이 가장 쉽습니다.

예를 들어, 화학 시뮬레이션을 수행할 때 양자 알고리즘에는 대규모 분자 궤도 상호 작용 적분 표가 필요합니다.
일반적으로 이러한 데이터는 알고리즘을 실행할 때 제공되는 파일에서 읽어옵니다.
Q#에는 파일 시스템에 액세스하는 메커니즘이 없으므로 이러한 종류의 데이터는 클래식 드라이버에서 가장 잘 수집되며, 수집된 이후 에 양자 알고리즘의 `Run` 메서드에 전달됩니다.

클래식 드라이버가 주요 역할을 수행하는 또 다른 경우는 변분 방식입니다.
이 알고리즘 클래스에서 양자 상태는 일부 클래식 매개 변수를 기준으로 준비되며, 해당 상태를 사용하여 몇 가지 중요한 값을 계산합니다.
이 매개 변수는 특정 유형의 언덕 오르기 또는 기계 학습 알고리즘에 따라 조정되며 양자 알고리즘이 다시 실행됩니다.
이러한 알고리즘의 경우 언덕 오르기 알고리즘 자체는 기존 드라이버에서 호출하는 순수한 클래식 함수로 구현하는 것이 가장 좋습니다. 그러면 언덕 오르기의 결과가 다음 번에 양자 알고리즘을 실행할 때 전달됩니다.

### <a name="running-the-quantum-algorithm"></a>양자 알고리즘 실행

이 부분은 일반적으로 매우 간단합니다.
각 Q# 연산은 정적 `Run` 메서드를 제공하는 클래스로 컴파일됩니다.
이 메서드에 대한 인수는 연산 자체의 병합된 인수 튜플과, 실행할 시뮬레이터에 해당하는 첫 번째 추가 인수를 사용하여 지정됩니다. 명명된 `(a: String, (b: Double, c: Double))` 형식의 튜플을 예상하는 연산에서 병합된 상대 튜플의 형식은 `(String a, Double b, Double c)`입니다.


`Run` 메서드에 인수를 전달할 때는 다음과 같은 미묘한 차이가 있습니다.

* 배열을 `Microsoft.Quantum.Simulation.Core.QArray<T>` 개체에 래핑해야 합니다.
    `QArray` 클래스에는 순서가 지정된 적절한 개체 컬렉션(`IEnumerable<T>`)을 사용할 수 있는 생성자가 있습니다.
* Q#에서 빈 튜플 `()`은 C#에서는 `QVoid.Instance`로 표시됩니다.
* 비어 있지 않은 튜플은 .NET `ValueType` 인스턴스로 표시됩니다.
* Q# 사용자 정의 형식은 기본 형식으로 전달됩니다.
* 연산 또는 함수를 `Run` 메서드에 전달하려면 시뮬레이터의 `Get<>` 메서드를 사용하여 연산 또는 함수의 클래스 인스턴스를 가져와기 때문입니다.

### <a name="processing-the-results"></a>결과 처리

양자 알고리즘의 결과는 `Run` 메서드에서 반환됩니다.
`Run` 메서드는 비동기적으로 실행되므로 <xref:System.Threading.Tasks.Task`1>의 인스턴스를 반환합니다.
실제 연산의 결과를 가져오는 방법에는 여러 가지가 있습니다. 가장 간단한 방법은 `Task`의 [`Result` 속성](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result)을 사용하는 것입니다.

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
그러나  [`Wait` 메서드](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) 또는 C# [`await` 키워드](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await)를 사용하는 것과 같은 다른 기법도 가능합니다.

인수를 사용할 때와 마찬가지로 Q# 튜플은 `ValueTuple` 인스턴스로 표시되고 Q# 배열은 `QArray` 인스턴스로 표시됩니다.
사용자 정의 형식은 기본 형식으로 반환됩니다.
빈 튜플 `()`는 `QVoid` 클래스의 인스턴스로 반환됩니다.

많은 양자 알고리즘은 유용한 답변을 파생하기 위해 상당한 사후 처리가 필요합니다.
예를 들어 Shor 알고리즘의 양자 부분은 한 숫자의 인수를 찾아내는 계산의 시작에 불과합니다.

대부분의 경우 클래식 드라이버에서 이러한 종류의 사후 처리를 수행하는 것이 가장 간단하고 쉽습니다.
클래식 드라이버만 사용자에게 결과를 보고하거나 디스크에 쓸 수 있습니다.
클래식 드라이버는 Q#에 표시되지 않는 분석 라이브러리 및 기타 수학 함수에 액세스할 수 있습니다.


## <a name="failures"></a>오류

연산을 실행하는 동안 Q# `fail` 문에 도달하면 `ExecutionFailException`이 throw됩니다.

`Run` 메서드에서 `System.Task`를 사용하기 때문에 `fail` 문의 결과로 throw되는 예외는 `System.AggregateException`에 래핑됩니다.
오류의 실제 원인을 찾으려면 `AggregateException` 
`InnerExceptions`를 반복해야 합니다. 예를 들면 다음과 같습니다.

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a>기타 클래식 언어

제공된 샘플은 C#, F# 및 Python으로 작성된 것이지만, Quantum Development Kit는 다른 언어로 작성된 클래식 호스트 프로그램 작성도 지원합니다.
예를 들어, Visual Basic에서 호스트 프로그램을 작성하려는 경우에는 [문제가 없이 잘 작동합니다](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).
