---
title: Q# 프로그램 테스트 및 디버깅
description: 단위 테스트, 사실 및 어설션을 사용하고 함수를 덤프하여 양자 프로그램을 테스트하고 디버깅하는 방법을 알아봅니다.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030585"
---
# <a name="testing-and-debugging"></a>테스트 및 디버깅

클래식 프로그래밍과 마찬가지로 양자 프로그램이 의도한 대로 작동하도록 하고 잘못된 양자 프로그램을 진단할 수 있어야 합니다.
이 섹션에서는 양자 프로그램을 테스트하고 디버깅하기 위해 Q#에서 제공하는 도구를 다룹니다.

## <a name="unit-tests"></a>단위 테스트

클래식 프로그램을 테스트하는 한 가지 일반적인 방법은 라이브러리에서 코드를 실행하는 *단위 테스트라는* 작은 프로그램을 작성하고 출력을 일부 예상 출력과 비교하는 것입니다.
예를 들어$ 2 ^2 `Square(2)` `4`= 4 $라는 *선험을* 알고 있기 때문에 반환을 보장할 수 있습니다.

Q#은 양자 프로그램에 대한 단위 테스트 생성을 지원하며 [xUnit](https://xunit.github.io/) 단위 테스트 프레임워크 내에서 테스트로 실행할 수 있습니다.

### <a name="creating-a-test-project"></a>테스트 프로젝트 만들기

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Visual Studio 2019를 엽니다. 메뉴로 `File` 이동하여 `New`  >  `Project...`을 선택합니다.
오른쪽 상단 모서리에서 `Q#`을 검색하고 `Q# Test Project` 템플릿을 선택합니다.

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

즐겨 찾는 명령줄에서 다음 명령을 실행합니다.
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

새 프로젝트에는 새 Q# 단위 테스트를 정의할 수 있는 편리한 위치를 제공하는 단일 파일이 `Tests.qs`있습니다.
처음에이 파일에는 새로 `AllocateQubit` 할당 된 큐빗이 $\ket{0}$ 상태에 있는지 확인하고 메시지를 인쇄하는 하나의 샘플 단위 테스트가 포함되어 있습니다.

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:new: 형식 `Unit` 및 반환인수를 `Unit` 취하는 모든 Q# 작업 또는 함수는 `@Test("...")` 특성을 통해 단위 테스트로 표시될 수 있습니다. `"QuantumSimulator"` 위의 해당 특성에 대한 인수는 테스트가 실행되는 대상을 지정합니다. 단일 테스트는 여러 대상에서 실행할 수 있습니다. 예를 들어 위의 `@Test("ResourcesEstimator")` 특성을 추가합니다. `AllocateQubit` 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
파일을 저장하고 모든 테스트를 실행합니다. 이제 두 개의 단위 테스트가 있어야 합니다. 

Q# 컴파일러는 기본 제공 대상인 "QuantumSimulator", "ToffoliSimulator"및 "ResourcesEstimator"를 단위 테스트의 유효한 실행 대상으로 인식합니다. 사용자 지정 실행 대상을 정의하기 위해 정규화된 이름을 지정할 수도 있습니다. 

### <a name="running-q-unit-tests"></a>Q# 단위 테스트 실행

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

솔루션당 일회성 설정으로 메뉴로 이동하여 `Test` 을 `Test Settings`  >  `Default Processor Architecture`  >  `X64`선택합니다.

> [!TIP]
> Visual Studio의 기본 프로세서 아키텍처 설정은 각`.suo`솔루션에 대한 솔루션 옵션() 파일에 저장됩니다.
> 이 파일을 삭제하면 프로세서 아키텍처로 `X64` 다시 선택해야 합니다.

프로젝트를 빌드하고 메뉴로 `Test` 이동하여 `Windows`  >  `Test Explorer`을 선택합니다. `AllocateQubit``Not Run Tests` 테스트 목록에 표시됩니다. 이 `Run All` 개별 테스트를 선택하거나 실행하면 통과해야 합니다!

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

테스트를 실행하려면 프로젝트 폴더(포함된 `Tests.csproj`폴더)로 이동하여 명령을 실행합니다.

```bash
$ dotnet restore
$ dotnet test
```

다음과 유사한 결과가 표시됩니다.

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

단위 테스트는 이름 및/또는 실행 대상에 따라 필터링할 수 있습니다.

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

내장 함수에는 <xref:microsoft.quantum.intrinsic.message> 형식이 `(String -> Unit)` 있으며 진단 메시지를 만들 수 있습니다.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

테스트 탐색기에서 테스트를 실행하고 테스트를 클릭하면 테스트 실행에 대한 정보(통과/실패 상태, 경과 시간 및 "출력" 링크)가 패널에 표시됩니다. "출력" 링크를 클릭하면 테스트 출력이 새 창에서 열립니다.

![테스트 출력](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

각 테스트의 합격/불합격 상태는 에 `dotnet test`의해 콘솔에 인쇄됩니다.
실패한 테스트의 경우 오류를 진단하는 데 도움이 되는 출력도 콘솔에 인쇄됩니다.

***

## <a name="facts-and-assertions"></a>사실 및 어설션

Q#의 함수에는 _논리적_ 부작용이 없으므로 출력 유형이 빈 튜플인 `()` 함수를 실행하는 _다른 종류의_ 효과는 Q# 프로그램 내에서 관찰할 수 없습니다.
즉, 대상 컴퓨터는 이 누락이 다음 `()` Q# 코드의 동작을 수정하지 않는다는 보장과 함께 반환되는 함수를 실행하지 않도록 선택할 수 있습니다.
이렇게 하면 함수 `()` 반환(즉, `Unit`즉)은 어설션을 포함하고 논리를 Q# 프로그램에 디버깅하는 데 유용한 도구가 됩니다. 

간단한 예를 살펴보겠습니다.

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

여기서 키워드는 `fail` 계산이 진행되지 않아야 한다는 것을 나타내며 Q# 프로그램을 실행하는 대상 컴퓨터에서 예외를 발생시킵니다.
정의에 따르면 문에 도달한 후 더 이상 Q# 코드가 실행되지 않도록 `fail` Q#내에서 이러한 종류의 오류를 관찰할 수 없습니다.
따라서, 우리가 에 전화를 `PositivityFact`지나 가면 , 우리는 입력이 긍정적이었다는 것을 확신 할 수 있습니다.

네임스페이스에서 `PositivityFact` [`Fact`](xref:microsoft.quantum.diagnostics.fact) 함수를 사용하는 것과 동일한 <xref:microsoft.quantum.diagnostics> 동작을 구현할 수 있습니다.

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

반면 *어설션은*사실과 유사하게 사용되지만 대상 컴퓨터의 상태에 따라 달라질 수 있습니다. 이에 상응하여 작업으로 정의되는 반면 팩트는 함수(위와 같이)로 정의됩니다.
이러한 차이점을 이해하려면 어설션 내에서 팩트를 다음과 같은 용도로 사용하는 것을 고려하십시오.

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

여기서는 작업을 <xref:microsoft.quantum.environment.getqubitsavailabletouse> 사용하여 사용할 수 있는 큐빗 수를 반환합니다.
이는 프로그램의 전역 상태와 실행 환경에 따라 명확히 달라지므로 당사의 `AssertQubitsAreAvailable` 정의도 작업이어야 합니다.
그러나 해당 전역 상태를 사용하여 `Bool` `Fact` 함수에 대한 입력으로 간단한 값을 생성할 수 있습니다.

이러한 아이디어를 [기반으로, 전주곡은](xref:microsoft.quantum.libraries.standard.prelude) 두 가지 특히 <xref:microsoft.quantum.intrinsic.assert> <xref:microsoft.quantum.intrinsic.assertprob> 유용한 어설션을 `()`제공하며, 둘 다 에 대한 작업으로 모델링됩니다. 이러한 주장은 각각 관심의 특정 측정을 설명하는 Pauli 연산자, 측정이 수행될 양자 레지스터 및 가상의 결과를 취합니다.
시뮬레이션에 의해 작동하는 대상 기계에서는 [복제 정리 없음에](https://en.wikipedia.org/wiki/No-cloning_theorem)구속되지 않으며 이러한 어설션에 전달된 레지스터를 방해하지 않고 이러한 측정을 수행할 수 있습니다.
그런 다음 시뮬레이터는 위의 `PositivityFact` 함수와 마찬가지로 가상의 결과가 실제로 관찰되지 않는 경우 계산을 중단할 수 있습니다.

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

복제 가용되지 않는 정리가 양자 상태의 검사를 방지하는 물리적 양자 `Assert` 하드웨어에서는 다른 효과없이 작업과 `AssertProb` 작업이 반환됩니다. `()`

네임 스페이스는 <xref:microsoft.quantum.diagnostics> 우리가 더 `Assert` 고급 조건을 확인할 수 있도록 가족의 몇 가지 더 많은 기능을 제공합니다. 

## <a name="dump-functions"></a>덤프 함수

양자 프로그램 문제 해결을 <xref:microsoft.quantum.diagnostics> 돕기 위해 네임스페이스는 대상 컴퓨터의 <xref:microsoft.quantum.diagnostics.dumpmachine> 현재 상태를 파일에 <xref:microsoft.quantum.diagnostics.dumpregister>덤프할 수 있는 두 가지 기능을 제공합니다. 각각의 생성된 출력은 대상 컴퓨터에 따라 다릅니다.

### <a name="dumpmachine"></a>DumpMachine

양자 개발 키트의 일부로 배포 된 전체 상태 양자 시뮬레이터는 파일 전체에 전체 양자 시스템의 [웨이브 함수를](https://en.wikipedia.org/wiki/Wave_function) 기록, 복잡한 숫자의 1 차원 배열로, 각 요소는 계산 기준 상태를 측정 할 확률의 진폭을 나타내는 $\ket{n}, 여기서 $\ket{n} = {b_{b_{n-1}... b_1b_0$b_i 비트에\{대해\}$b_i. 예를 들어, 양자 상태에서 $${1}\begin{align} \ frac {\sqrt{2}} \\frac{{(1{00} + i)}{2} \ket{10}, \end{align} $$ 호출이 <xref:microsoft.quantum.diagnostics.dumpmachine> 할당된 컴퓨터에서 는 이 출력을 생성합니다.

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

첫 번째 행은 해당 큐빗의 해당 큐빗의 주요 순서로 주석을 제공합니다.
나머지 행은 카르테시안 및 극성 형식 모두에서 기본 상태 벡터 $\ket{n}$를 측정하는 확률 진폭을 설명합니다. 첫 번째 행에 대한 자세한 내용은 다음과 같은

* **`∣0❭:`** 이 행은 `0` 계산 기준 상태에 해당합니다.
* **`0.707107 +  0.000000 i`**: 카르테시안 형식의 확률 진폭입니다.
* **` == `**: `equal` 부호는 두 동등한 표현을 분리합니다.
* **`**********  `**: 크기의 그래픽 표현, 개수는 `*` 이 상태 벡터를 측정할 확률에 비례한다.
* **`[ 0.500000 ]`**: 크기의 숫자 값
* **`    ---`**: 진폭의 위상에 대한 그래픽 표현입니다(아래 참조).
* **`[ 0.0000 rad ]`**: 위상의 숫자 값(라디안)입니다.

크기와 위상모두 그래픽 표현으로 표시됩니다. 크기 표현은 직선입니다: 막대가 `*`표시될 확률이 클수록 막대가 커집니다. 위상에 대 한 범위에 따라 각도를 나타내는 다음 기호를 표시 합니다.

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

다음 예제는 `DumpMachine` 몇 가지 일반적인 상태에 대해 보여 준다.

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > 큐빗의 ID는 런타임에 할당되며 큐빗이 할당된 순서 또는 큐빗 레지스터 내의 위치와 반드시 일치하지는 않습니다.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > 예를 들어 코드에 중단점을 배치하고 qubit 변수의 값을 검사하여 Visual Studio에서 qubit ID를 파악할 수 있습니다.
  > 
  > ![비주얼 스튜디오에서 큐비트 ID 표시](~/media/qubit_id.png)
  >
  > `0` 인덱스가 `register2` 있는 큐빗에는`3`id=가 있으며 `1` 인덱스가`2`있는 큐빗에는 id=가 있습니다.

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > 예를 들어 <xref:microsoft.quantum.intrinsic.message> 함수를 사용하고 메시지에서 qubit 변수를 전달하여 qubit ID를 알아낼 수 있습니다.
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > 이 출력을 생성할 수 있습니다.
  >```
  > 0=q:3; 1=q:2
  >```
  > 즉, 인덱스가 `0` `register2` 있는 큐비트에`3`id=, 인덱스가 `1` 있는`2`큐비트에는 id=가 있습니다.


***

<xref:microsoft.quantum.diagnostics.dumpmachine><xref:microsoft.quantum.diagnostics> 네임스페이스의 일부이므로 사용하려면 `open` 문을 추가해야 합니다.

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a>DumpRegister

<xref:microsoft.quantum.diagnostics.dumpregister>정보 <xref:microsoft.quantum.diagnostics.dumpmachine>양을 해당 큐빗과 관련된 정보로만 제한하는 큐빗 배열을 제외하면 작동합니다.

와 <xref:microsoft.quantum.diagnostics.dumpmachine>마찬가지로, 생성 <xref:microsoft.quantum.diagnostics.dumpregister> 된 정보는 대상 컴퓨터에 따라 달라집니다. 풀 스테이트 양자 시뮬레이터의 경우 제공된 양자 서브 시스템의 글로벌 단계까지 웨이브 함수를 파일에 기록하여 <xref:microsoft.quantum.diagnostics.dumpmachine>동일한 형식으로 제공된 큐빗에 의해 생성됩니다.  {1}예를 들어, 양자 상태에서 $$ \begin{align} = \frac {\sqrt{2}} \ket{00} - \frac{{(1 + i)}{2} \ket{10} = - e^{-i\pi/4에 할당된 두 개의{1}큐비트만 있는{2}기계를{0} 다시 가져가라. } (\frac{1} {\sqrt } \ket - \frac{{(1{2}+{0} i)} <xref:microsoft.quantum.diagnostics.dumpregister> {2} \otimes \frac{-(1 + i)}{\sqrt } \ket) \ end{align} $$ 이 출력을 생성하기 위해 `qubit[0]` 호출:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<xref:microsoft.quantum.diagnostics.dumpregister> 호출은 `qubit[1]` 이 출력을 생성합니다.

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

일반적으로 다른 레지스터와 얽혀 있는 레지스터의 상태는 순수 상태가 아닌 혼합 상태입니다. 이 경우 <xref:microsoft.quantum.diagnostics.dumpregister> 다음 메시지를 출력합니다.

```
Qubits provided (0;) are entangled with some other qubit.
```

다음 예제에서는 Q# 코드와 <xref:microsoft.quantum.diagnostics.dumpregister> <xref:microsoft.quantum.diagnostics.dumpmachine> 둘 다 사용하는 방법을 보여 줍니다.

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a>디버깅

`Dump` 기능 및 `Assert` 작업 외에도 Q#은 표준 Visual Studio 디버깅 기능의 하위 집합인 [줄 중단점 설정,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [F10을 사용한 코드 단계별 단계](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) 및 [클래식 변수의 값 검사는](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) 시뮬레이터에서 코드 실행 중에 모두 가능합니다.

Visual Studio 코드에서 디버깅은 OmniSharp에서 제공하는 Visual Studio 코드 확장용 C#에서 제공하는 디버깅 기능을 활용하며 [최신 버전을](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)설치해야 합니다. 
