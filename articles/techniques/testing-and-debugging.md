---
title: '테스트 및 디버그 Q # 프로그램'
description: 단위 테스트, 팩트 및 어설션을 사용 하는 방법 및 덤프 함수를 사용 하 여 퀀텀 프로그램을 테스트 하 고 디버그 하는 방법을 알아봅니다.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 3df8df8defabcc9cc87d59f543f425c882b001e0
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907684"
---
# <a name="testing-and-debugging"></a>테스트 및 디버깅

기존 프로그래밍과 마찬가지로 퀀텀 프로그램이 의도 한 대로 작동 하는지 확인 하 고 잘못 된 퀀텀 프로그램을 진단할 수 있어야 합니다.
이 섹션에서는 퀀텀 프로그램 테스트 및 디버깅을 위해 Q #에서 제공 하는 도구를 다룹니다.

## <a name="unit-tests"></a>단위 테스트

클래식 프로그램을 테스트 하는 일반적인 방법 중 하나는 라이브러리에서 코드를 실행 하 고 해당 출력을 예상 출력과 비교 하는 *단위 테스트* 라는 작은 프로그램을 작성 하는 것입니다.
예를 들어 $2 ^ 2 = $4 *apriori* 을 알고 있으므로 `Square(2)`에서 `4`를 반환 하도록 할 수 있습니다.

Q #은 퀀텀 프로그램에 대 한 단위 테스트 만들기를 지원 하 고 [Xunit](https://xunit.github.io/) 단위 테스트 프레임 워크 내에서 테스트로 실행 될 수 있습니다.

### <a name="creating-a-test-project"></a>테스트 프로젝트 만들기

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Visual Studio 2019를 엽니다. `File` 메뉴로 이동 하 여 `New` > `Project...`를 선택 합니다.
오른쪽 위 모서리에서 `Q#`을 검색 하 고 `Q# Test Project` 템플릿을 선택 합니다.

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

선호 하는 명령줄에서 다음 명령을 실행 합니다.
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

새 프로젝트에는 새 Q # 단위 테스트를 정의 하는 데 편리한 장소를 제공 하는 단일 파일 `Tests.qs`포함 됩니다.
처음에이 파일에는 새로 할당 된 \ket가 ${0}$ 상태에 있는지 확인 하 고 메시지를 인쇄 하는 하나의 샘플 단위 테스트 `AllocateQubit` 포함 되어 있습니다.

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

: new: `Unit` 형식의 인수를 사용 하 고 `Unit`를 반환 하는 모든 Q # 작업 또는 함수는 `@Test("...")` 특성을 통해 단위 테스트로 표시 될 수 있습니다. 위의 `"QuantumSimulator"` 해당 특성에 대 한 인수는 테스트가 실행 되는 대상을 지정 합니다. 단일 테스트를 여러 대상에서 실행할 수 있습니다. 예를 들어 `AllocateQubit`위의 `@Test("ResourcesEstimator")` 특성을 추가 합니다. 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
파일을 저장 하 고 모든 테스트를 실행 합니다. 이제 두 개의 단위 테스트가 있습니다. 여기에는 AllocateQuantumSimulator 비트가 실행 되 고 하나는 ResourceEstimator에서 실행 됩니다. 

Q # 컴파일러는 기본 제공 대상 "QuantumSimulator", "ToffoliSimulator" 및 "ResourcesEstimator"를 단위 테스트에 대 한 올바른 실행 대상으로 인식 합니다. 또한 사용자 지정 실행 대상을 정의 하는 정규화 된 이름을 지정할 수 있습니다. 

### <a name="running-q-unit-tests"></a>Q # 단위 테스트 실행

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

솔루션 당 일회성 설치로 `Test` 메뉴로 이동 하 여 `Test Settings` > `Default Processor Architecture` > `X64`를 선택 합니다.

> [!TIP]
> Visual Studio의 기본 프로세서 아키텍처 설정은 각 솔루션에 대 한 솔루션 옵션 (`.suo`) 파일에 저장 됩니다.
> 이 파일을 삭제 하는 경우 프로세서 아키텍처로 `X64`을 다시 선택 해야 합니다.

프로젝트를 빌드하고 `Test` 메뉴로 이동 하 여 `Windows` > `Test Explorer`를 선택 합니다. `AllocateQubit` `Not Run Tests` 그룹의 테스트 목록에 표시 됩니다. `Run All`를 선택 하거나이 개별 테스트를 실행 하 고 통과 해야 합니다.

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

테스트를 실행 하려면 프로젝트 폴더 (`Tests.csproj`포함 된 폴더)로 이동 하 고 명령을 실행 합니다.

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

단위 테스트는 이름 및/또는 실행 대상에 따라 필터링 할 수 있습니다.

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

내장 함수 <xref:microsoft.quantum.intrinsic.message>에는 `(String -> Unit)` 형식이 있으며 진단 메시지를 만들 수 있습니다.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

테스트 탐색기에서 테스트를 실행 하 고 테스트를 클릭 하면 테스트 실행: 성공/실패 상태, 경과 시간 및 "출력" 링크에 대 한 정보가 포함 된 패널이 표시 됩니다. "출력" 링크를 클릭 하면 테스트 출력이 새 창에서 열립니다.

![테스트 출력](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

각 테스트에 대 한 통과/실패 상태는 `dotnet test`하 여 콘솔에 출력 됩니다.
실패 한 테스트의 경우 출력은 오류를 진단 하는 데 도움이 되도록 콘솔에도 출력 됩니다.

***

## <a name="facts-and-assertions"></a>팩트 및 어설션

Q #의 함수에는 _논리적인_ 부작용이 없으므로 출력 형식이 빈 튜플 인 함수를 실행 하는 _다른 종류_ 의 효과는 Q # 프로그램 내에서 관찰 될 수 `()`.
즉, 대상 컴퓨터는 이러한 누락으로 인 한 `()` 반환 하는 함수를 실행 하지 않도록 선택할 수 있습니다 .이는 다음 Q # 코드의 동작을 수정 하지 않습니다.
이를 통해 함수는 `()` (즉, `Unit`)을 반환 하는 유용한 도구를 Q # 프로그램에 포함 시킬 수 있습니다. 

간단한 예제를 살펴보겠습니다.

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

여기서 키워드 `fail`는 계산이 진행 되지 않아야 함을 나타냅니다. Q # 프로그램을 실행 하는 대상 컴퓨터에서 예외가 발생 합니다.
정의에 따라 Q # 내에서 이러한 종류의 오류를 확인할 수 없습니다. `fail` 문에 도달한 후에 추가 Q # 코드가 실행 되지 않습니다.
따라서 `PositivityFact`에 대 한 호출을 계속 진행 하는 경우 해당 입력이 양수가 되도록 보장할 수 있습니다.

<xref:microsoft.quantum.diagnostics> 네임 스페이스의 [`Fact`](xref:microsoft.quantum.diagnostics.fact) 함수를 사용 하 `PositivityFact`와 동일한 동작을 구현할 수 있습니다.

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

반면에 *어설션은*팩트와 유사 하 게 사용 되지만 대상 컴퓨터의 상태에 따라 달라질 수 있습니다. 이와 마찬가지로 팩트는 작업으로 정의 되는 반면 팩트는 위에 나와 있는 함수로 정의 됩니다.
구분을 이해 하려면 어설션 내에서 다음과 같은 팩트를 사용 하는 것이 좋습니다.

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

여기서는 작업 <xref:microsoft.quantum.environment.getqubitsavailabletouse>를 사용 하 여 사용할 수 있는 해당 비트 수를 반환 합니다.
이는 프로그램의 전역 상태와 해당 실행 환경에 따라 달라 지므로 `AssertQubitsAreAvailable`의 정의도 작업 이어야 합니다.
그러나이 전역 상태를 사용 하 여 간단한 `Bool` 값을 `Fact` 함수의 입력으로 생성할 수 있습니다.

이러한 아이디어를 기반으로 하 [는 prelude는](xref:microsoft.quantum.libraries.standard.prelude) <xref:microsoft.quantum.intrinsic.assert> <xref:microsoft.quantum.intrinsic.assertprob> `()`에 대 한 작업으로 모델링 된 두 가지 특히 유용한 어설션을 제공 합니다. 이러한 어설션은 각각 특정 측정값을 설명 하는 Pauli 연산자, 측정을 수행 해야 하는 퀀텀 레지스터 및 가상 결과를 사용 합니다.
시뮬레이션을 통해 작동 하는 대상 컴퓨터에서는 [복제 안 함 정리](https://en.wikipedia.org/wiki/No-cloning_theorem)바인딩되지 않으며 이러한 어설션에 전달 된 레지스터를 방해 하지 않고 이러한 측정을 수행할 수 있습니다.
그런 다음 시뮬레이터는 위의 `PositivityFact` 함수와 마찬가지로 가상 결과가 실제로 관찰 되지 않는 경우 계산을 중단 합니다.

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

복제 안 함 정리에서 퀀텀 상태를 검사 하는 것을 방지 하는 실제 퀀텀 하드웨어에서는 `Assert` 및 `AssertProb` 작업이 다른 효과 없이 `()` 반환 됩니다.

<xref:microsoft.quantum.diagnostics> 네임 스페이스는 더 많은 고급 조건을 확인할 수 있도록 하는 `Assert` 패밀리의 여러 기능을 제공 합니다. 

## <a name="dump-functions"></a>덤프 함수

퀀텀 프로그램의 문제를 해결 하는 데 도움이 되도록 <xref:microsoft.quantum.diagnostics> 네임 스페이스는 대상 컴퓨터의 현재 상태 (<xref:microsoft.quantum.diagnostics.dumpmachine> 및 <xref:microsoft.quantum.diagnostics.dumpregister>)를 파일에 덤프할 수 있는 두 가지 함수를 제공 합니다. 각각의 생성 된 출력은 대상 컴퓨터에 따라 다릅니다.

### <a name="dumpmachine"></a>DumpMachine

퀀텀 개발 키트의 일부분으로 배포 되는 전체 상태 퀀텀 시뮬레이터는 전체 퀀텀 시스템의 [wave 함수](https://en.wikipedia.org/wiki/Wave_function) 를 파일에 기록 하 고, 각 요소가 계산 기준 상태 $ \ket{n} $를 측정할 확률의 진폭을 나타냅니다. 여기서 $ \ket{n} = \ket{b_ {n-1} ... bits $\{에 대 한 b_1b_0} $ b_i\}$. 예를 들어, 두 개의 om비트만 할당 된 컴퓨터에서 및 퀀텀 상태 $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10}, \end{align} $ $ 호출은이 출력을 생성 합니다.<xref:microsoft.quantum.diagnostics.dumpmachine>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

첫 번째 행은 중요 한 순서 대로 해당 하는의 Id를 사용 하 여 주석을 제공 합니다.
나머지 행은 데카르트 및 극좌표 형식의 기본 상태 vector $ \ket{n} $를 측정 하는 확률 진폭을 설명 합니다. 첫 번째 행에 대해 자세히 설명 합니다.

* 이 행 **`∣0❭:`** `0` 계산 기준 상태에 해당 합니다.
* **`0.707107 +  0.000000 i`** : 데카르트 형식의 확률 진폭입니다.
* **` == `** : `equal` seperates 부호와 동일 하 게 표현 됩니다.
* **`**********  `** : 크기의 그래픽 표현으로, `*` 수는이 상태 벡터를 측정할 확률에 비례 합니다.
* **`[ 0.500000 ]`** : 크기의 숫자 값입니다.
* **`    ---`** : 진폭의 단계 (아래 참조)에 대 한 그래픽 표현입니다.
* **`[ 0.0000 rad ]`** : 단계의 숫자 값 (라디안 단위)입니다.

크기와 단계가 모두 그래픽 표현으로 표시 됩니다. 크기 표현은 간단 하 게 표시 됩니다 .이는 `*`막대를 표시 하 고 막대의 클수록 표시 되는 확률이 큽니다. 단계에서는 범위에 따라 각도를 나타내기 위해 다음 기호를 표시 합니다.

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

다음 예에서는 몇 가지 일반적인 상태에 대 한 `DumpMachine` 보여 줍니다.

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
  > 의 id는 런타임에 할당 되며,이는 해당 비트를 할당 하는 순서 또는이를 사용 하는 순서에 따라 결정 되는 것은 아닙니다.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > 코드에 중단점을 배치 하 고 다음과 같이 다음과 같이 Visual Studio에서 사용자 비트 id를 확인할 수 있습니다.
  > 
  > ![Visual Studio에서 이상 비트 id 표시](~/media/qubit_id.png)
  >
  > `register2`에서 index가 `0` 인 이상 비트에는 id =`3`, 인덱스 `1`의 고 비트는 id =`2`입니다.

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > <xref:microsoft.quantum.intrinsic.message> 함수를 사용 하 고 다음과 같이 메시지에 다음과 같은 기능을 전달 하 여이에 대 한 비트 id를 알아낼 수 있습니다.
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > 다음 출력이 생성 될 수 있습니다.
  >```
  > 0=q:3; 1=q:2
  >```
  > 즉, 인덱스를 사용 하 여 `register2`에서 `0` 하는 것이 id =`3`이며 인덱스 `1`의 이상 비트는 id =`2`입니다.


***

<xref:microsoft.quantum.diagnostics.dumpmachine> <xref:microsoft.quantum.diagnostics> 네임 스페이스에 포함 되어 있으므로이를 사용 하려면 `open` 문을 추가 해야 합니다.

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

<xref:microsoft.quantum.diagnostics.dumpregister>은 (는) <xref:microsoft.quantum.diagnostics.dumpmachine>와 같이 작동 합니다. 단,이는 해당 하는 것과 관련 된 정보만으로 정보의 양을 제한 하는 데 사용 됩니다.

<xref:microsoft.quantum.diagnostics.dumpmachine>와 마찬가지로 <xref:microsoft.quantum.diagnostics.dumpregister>에 의해 생성 되는 정보는 대상 컴퓨터에 따라 다릅니다. 전체 상태 퀀텀 시뮬레이터에 대해 wave 함수를 파일에 기록 합니다 .이 함수는 <xref:microsoft.quantum.diagnostics.dumpmachine>와 동일한 형식으로 제공 된이를 통해 생성 된 퀀텀 하위 시스템의 전역 단계까지 파일에 기록 합니다.  예를 들어 두 개의 om비트만 할당 된 컴퓨터를 다시 사용 하 고 퀀텀 상태 $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10} =-e ^ {-i \ pi/4} ((\frac{1}{\sqrt{2}} \ket{0}-\frac{(1 + i)}{2} \ket{1}) \frac \frac{-(1 + i)} {\sqrt{2}} \ket{0}), \end{align} $ $ `qubit[0]`에 대 한 호출 <xref:microsoft.quantum.diagnostics.dumpregister>이 출력을 생성 합니다. :

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

`qubit[1]`에 대 한 <xref:microsoft.quantum.diagnostics.dumpregister>를 호출 하면 다음 출력이 생성 됩니다.

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

일반적으로 다른 레지스터와 함께 사용 되는 레지스터의 상태는 순수 상태가 아닌 혼합 된 상태입니다. 이 경우 <xref:microsoft.quantum.diagnostics.dumpregister>는 다음과 같은 메시지를 출력 합니다.

```
Qubits provided (0;) are entangled with some other qubit.
```

다음 예제에서는 Q # 코드에서 <xref:microsoft.quantum.diagnostics.dumpregister>와 <xref:microsoft.quantum.diagnostics.dumpmachine>를 모두 사용 하는 방법을 보여 줍니다.

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

`Assert` 및 `Dump` 함수 및 작업을 기반으로 하는 Q #은 표준 Visual Studio 디버깅 기능의 하위 집합을 지원 합니다. [줄 중단점 설정](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), F10 키를 [사용 하 여 코드 단계별](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) 실행 및 [클래식 변수의 값 검사](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) 는 모두 시뮬레이터에서 코드를 실행 하는 동안 가능 합니다.

Visual Studio Code 디버깅은 OmniSharp에서 제공 하는 C# Visual Studio Code 확장에 대해에서 제공 하는 디버깅 기능을 활용 하 고 [최신 버전](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)을 설치 해야 합니다. 
