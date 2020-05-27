---
title: Q#을 사용한 얽힘 살펴보기
description: Q#에서 양자 프로그램을 작성하는 방법을 알아봅니다. QDK(Quantum Development Kit)를 사용하여 Bell State 애플리케이션을 개발합니다.
author: natke
ms.author: nakersha
ms.date: 10/07/2019
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 7836e39227fa2282c6e2faa039f6e625103d5403
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426837"
---
# <a name="tutorial-explore-entanglement-with-q"></a>자습서: Q\#을 사용한 얽힘 살펴보기

이 자습서에서는 큐비트를 조작 및 측정하고 중첩과 얽힘의 효과를 시연하는 Q# 프로그램을 작성하는 방법을 보여 줍니다.
QDK를 설치하고, 프로그램을 빌드하여 양자 시뮬레이터에서 실행하는 방법을 안내합니다.  

양자 얽힘을 보여주는 벨이라는 애플리케이션을 작성합니다.
벨이라는 이름은 가장 간단한 중첩과 양자 얽힘의 예를 표현하는 데 사용되는 두 큐비트의 특정 양자 상태를 의미하는 벨 상태에서 따온 것입니다.

## <a name="pre-requisites"></a>필수 구성 요소

코딩을 시작할 준비가 되면 계속하기 전에 다음 단계를 수행합니다. 

* 기본 설정 언어와 개발 환경을 사용하여 Quantum Development Kit를 [설치](xref:microsoft.quantum.install)합니다.
* QDK가 이미 설치되어 있는 경우 최신 버전으로 [업데이트](xref:microsoft.quantum.update)해야 합니다.

QDK를 설치하지 않고 설명에 따라 Q# 프로그래밍 언어와 양자 컴퓨팅의 첫 번째 개념을 검토할 수도 있습니다.

## <a name="demonstrating-qubit-behavior-with-q"></a>Q#에서 큐비트 동작 시연

간단한 [큐비트 정의](xref:microsoft.quantum.overview.understanding)를 떠올려 보세요.  클래식 비트는 0 또는 1 같은 단일 이진 값을 보유하는 반면, 큐비트 상태는 0과 1의 동시 **중첩**일 수 있습니다.  개념적으로 큐비트는 공간의 방향(벡터라고도 함)이라고 생각할 수 있습니다.  가능한 모든 방향은 큐비트가 될 수 있습니다. 두 **클래식 상태**는 두 방향입니다. 즉, 0을 측정할 확률이 100%이고, 1을 측정할 확률이 100%입니다.  또한 이 표현은 [블로흐 구](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere)를 통해 보다 형식적으로 시각화됩니다.


측정 작업은 이진 결과를 생성하고 큐비트 상태를 변경합니다. 측정은 이진 값(0 또는 1)을 생성합니다.  큐비트는 중첩(모든 방향)에서 클래식 상태 중 하나로 변경됩니다.  그 후 개입 작업 없이 동일한 측정을 반복하여 동일한 이진 결과를 생성합니다.  

여러 큐비트가 서로 **얽힐** 수 있습니다. 얽힌 큐비트 하나를 측정하면 다른 큐비트의 상태 정보도 업데이트됩니다.

이제 Q#에서 이 동작을 어떻게 표현하는지 시연할 준비가 되었습니다.  가능한 가장 간단한 프로그램으로 시작하여 양자 중첩 및 양자 얽힘을 보여주는 프로그램을 빌드합니다.

## <a name="setup"></a>설치 프로그램

Microsoft의 Quantum Development Kit를 사용하여 개발된 애플리케이션은 다음 두 부분으로 구성됩니다.

1. 하나 이상의 양자 알고리즘 - Q# 양자 프로그래밍 언어를 사용하여 구현됩니다.
1. 호스트 프로그램 - Python 또는 C#과 같은 프로그래밍 언어로 구현되어 주 진입점 역할을 수행하고, Q# 연산을 호출하여 양자 알고리즘을 실행합니다.

#### <a name="python"></a>[Python](#tab/tabid-python)

1. 애플리케이션의 위치 선택

1. `Bell.qs`라는 파일을 만듭니다. 이 파일에는 Q# 코드가 포함됩니다.

1. `host.py`라는 파일을 만듭니다. 이 파일에는 Python 호스트 코드가 포함됩니다.

#### <a name="c-command-line"></a>[C# 명령줄](#tab/tabid-csharp)

1. 새 Q# 프로젝트를 만듭니다.

    ```bash
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    `.csproj` 파일, Q# 파일(`Operations.qs`) 및 호스트 프로그램 파일(`Driver.cs`)이 표시되어야 합니다.

1. Q# 파일 이름 바꾸기

    ```bash
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. 새 프로젝트 만들기

   * Visual Studio 열기
   * **파일** 메뉴로 이동하여 **새로 만들기** -> **프로젝트...** 를 차례로 선택
   * 프로젝트 템플릿 탐색기에서 검색 필드에 `Q#`을 입력하고 `Q# Application` 템플릿을 선택합니다.
   * 프로젝트 이름을 `Bell`로 바꾸기

1. Q# 파일 이름 바꾸기

   * **솔루션 탐색기**로 이동
   * 마우스 오른쪽 단추로 `Operations.qs` 파일 클릭
   * 이름을 `Bell.qs`로 바꾸기

* * *

## <a name="write-a-q-operation"></a>Q# 연산 작성

특정 양자 상태에 있는 두 큐비트를 준비하고, Q#에서 두 큐비트의 상태를 변경하는 작업을 수행하고 중첩 및 얽힘의 효과를 보여주는 것이 우리의 목표입니다. 큐비트 상태, 작업 및 측정을 보여주는 연산을 하나씩 작성하겠습니다.

**개요:**  아래의 첫 번째 코드에서는 Q#에서 큐비트를 작업하는 방법을 보여줍니다.  큐비트 상태를 변환하는 `M` 및 `X` 연산을 소개합니다. 

이 코드 조각에서 `Set` 연산은 큐비트를 매개 변수로 사용하고 또 다른 매개 변수 `desired`를 사용하여 우리가 원하는 큐비트 상태를 나타내는 것으로 정의됩니다.  `Set` 연산은 `M` 연산을 사용하여 큐비트를 측정합니다.  Q#에서 큐비트 측정은 항상 `Zero` 또는 `One`을 반환합니다.  측정에서 반환된 값이 원하는 값과 일치하지 않으면 Set는 큐비트를 "대칭 이동"합니다. 즉, 큐비트 상태를 새로운 상태로 변경하는 `X` 연산을 실행합니다. 이 상태에서는 `Zero` 및 `One`을 반환하는 측정 확률이 반대입니다.  `Set` 연산의 효과를 보여주기 위해 `TestBellState` 연산이 추가됩니다.  이 연산은 `Zero` 또는 `One`을 입력으로 취하며, 이 입력을 사용하여 `Set` 연산을 몇 차례 호출하고, 큐비트 측정에서 `Zero`가 반환된 횟수와 `One`이 반환된 횟수를 집계합니다. 물론 `TestBellState` 연산의 첫 번째 시뮬레이션 출력에서는 `Zero`를 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `Zero`를 반환하고, `One`을 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `One`을 반환할 것으로 예상됩니다.  또한 중첩 및 얽힘을 보여주는 코드를 `TestBellState`에 추가할 것입니다.


### <a name="q-operation-code"></a>Q# 연산 코드

1. Bell.qs 파일의 내용을 다음 코드로 바꿉니다.

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    이제 이 연산을 호출하여 큐비트를 클래식 상태로 설정하면 항상 `Zero`를 반환하거나 항상 `One`을 반환할 수 있습니다.  `Zero` 및 `One`은 큐비트 측정에서 가능한 두 가지 결과를 나타내는 상수입니다.

    `Set` 연산은 큐비트를 측정합니다.
    큐비트가 현재 우리가 원하는 상태이면 `Set`는 큐비트를 그대로 둡니다. 그렇지 않으면 `X` 연산을 실행하여 큐비트를 원하는 상태로 변경합니다.

### <a name="about-q-operations"></a>Q# 연산 정보

Q# 연산은 양자 서브루틴입니다. 즉, 양자 연산을 포함하는 호출 가능 루틴입니다.

연산에 대한 인수는 괄호로 묶인 튜플로 지정됩니다.

연산의 반환 형식은 콜론 뒤에 지정됩니다. 이 경우 `Set` 연산에는 반환이 없으므로 `Unit`를 반환하는 것으로 표시됩니다. 이는 F#의 `unit`와 동일한 Q#이며, C#의 `void` 및 Python의 빈 튜플(`Tuple[()]`)과 거의 비슷합니다.

첫 번째 Q# 연산에서는 다음과 같은 두 개의 양자 연산을 사용했습니다.

* [M](xref:microsoft.quantum.intrinsic.m) 연산 - 큐비트의 상태를 측정합니다.
* [X](xref:microsoft.quantum.intrinsic.x) 연산 - 큐비트의 상태를 대칭 이동합니다.

양자 연산은 큐비트의 상태를 변환합니다. 가끔 사람들은 클래식 논리 게이트와 비슷하게, 연산 대신 양자 게이트에 대해 이야기합니다. 그 기원은 알고리즘이 이론적 아이디어에 불과했고 클래식 컴퓨팅의 회로 다이어그램과 유사한 다이어그램으로 시각화되던 양자 컴퓨팅 초기 시대입니다.

### <a name="add-q-test-code"></a>Q# 테스트 코드 추가

1. `Set` 연산이 끝난 후 다음 연산을 네임스페이스 내의 `Bell.qs` 파일에 추가합니다.

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    이 연산(`TestBellState`)은 `count` 반복에 대해 루프를 실행하고, 큐비트에 지정된 `initial` 값을 설정한 다음, 결과를 측정합니다(`M`). 측정한 0과 1의 개수에 대한 통계를 수집하여 호출자에게 반환합니다. 다른 필요한 연산을 수행합니다. 다른 사용자가 알려진 상태에서 이 큐비트를 할당할 수 있도록 반환하기 전에 해당 큐비트를 알려진 상태(`Zero`)로 다시 설정합니다. 이는 `using` 문에 필요합니다.

### <a name="about-variables-in-q"></a>Q#의 변수 정보

기본적으로 Q#의 변수는 변경할 수 없습니다. 바인딩된 후에는 해당 값이 변경되지 않을 수 있습니다. `let` 키워드는 변경할 수 없는 변수의 바인딩을 나타내는 데 사용됩니다. 연산 인수는 항상 변경할 수 없습니다.

예제의 `numOnes`와 같이 값이 변경될 수 있는 변수가 필요한 경우 `mutable` 키워드를 사용하여 해당 변수를 선언할 수 있습니다. 변경할 수 있는 변수의 값은 `set` 문을 사용하여 변경할 수 있습니다.

두 경우 모두에서 변수 형식은 컴파일러를 통해 유추됩니다. Q#에는 변수에 대한 형식 주석이 필요하지 않습니다.

### <a name="about-using-statements-in-q"></a>Q#의 `using` 문 정보

`using` 문은 Q#에서도 특수합니다. 코드 블록에서 사용할 큐비트를 할당하는 데 사용됩니다. Q#에서는 복잡한 알고리즘의 전체 수명 동안 유지되는 고정 리소스가 아니라 모든 큐비트가 동적으로 할당되고 해제됩니다. `using` 문은 시작 부분에서 큐비트 세트를 할당하고, 블록의 끝에서 해당 큐비트를 해제합니다.

## <a name="create-the-host-application-code"></a>호스트 애플리케이션 코드 만들기

#### <a name="python"></a>[Python](#tab/tabid-python)

1. `host.py` 파일을 열고 다음 코드를 추가합니다.

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

1. `Driver.cs` 파일의 내용을 다음 코드로 바꿉니다.

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a>호스트 애플리케이션 코드 정보

#### <a name="python"></a>[Python](#tab/tabid-python)

Python 호스트 애플리케이션은 다음 세 부분으로 구성됩니다.

* 양자 알고리즘에 필요한 인수를 계산합니다. 이 예제에서 `count`는 1,000으로 고정되고, `initial`은 큐비트의 초기 값입니다.
* 가져온 Q# 연산의 `simulate()` 메서드를 호출하여 양자 알고리즘을 실행합니다.
* 연산의 결과를 처리합니다. 이 예제에서 `res`는 연산 결과를 받습니다. 여기서 결과는 시뮬레이터에서 측정한 0(`num_zeros`)의 수와 1(`num_ones`)의 수에 대한 튜플입니다. 튜플을 분해하여 두 개의 필드를 가져오고, 결과를 출력합니다.

#### <a name="c"></a>[C#](#tab/tabid-csharp)

C# 호스트 애플리케이션은 다음 네 부분으로 구성됩니다.

* 양자 시뮬레이터를 생성합니다. 이 예제에서 `qsim`은 시뮬레이터입니다.
* 양자 알고리즘에 필요한 인수를 계산합니다. 이 예제에서 `count`는 1,000으로 고정되고, `initial`은 큐비트의 초기 값입니다.
* 양자 알고리즘을 실행합니다. 각 Q# 연산은 동일한 이름의 C# 클래스를 생성합니다. 이 클래스에는 **비동기적으로** 연산을 실행하는 `Run` 메서드가 있습니다. 실제 하드웨어에서 비동기적으로 실행되므로 실행이 비동기적입니다. `Run` 메서드는 비동기적이므로 `Result` 속성을 가져옵니다. 이 속성은 작업이 완료될 때까지 실행을 차단하고 결과를 동기적으로 반환합니다.
* 연산의 결과를 처리합니다. 이 예제에서 `res`는 연산 결과를 받습니다. 여기서 결과는 시뮬레이터에서 측정한 0(`numZeros`)의 수와 1(`numOnes`)의 수에 대한 튜플입니다. 이는 C#에서 ValueTuple로 반환됩니다. 튜플을 분해하여 두 개의 필드를 가져오고, 결과를 출력하고, 키 누름을 기다립니다.

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a>빌드 및 실행

#### <a name="python"></a>[Python](#tab/tabid-python)

1. 터미널에서 다음 명령을 실행합니다.

    ```
    python host.py
    ```

    이 명령은 Q# 연산을 시뮬레이션하는 호스트 애플리케이션을 실행합니다.

결과는 다음과 같아야 합니다.

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[명령줄/Visual Studio Code](#tab/tabid-csharp)

1. 터미널에서 다음을 실행합니다.

    ```bash
    dotnet run
    ```

    이 명령은 필요한 모든 패키지를 자동으로 다운로드하고, 애플리케이션을 빌드한 다음, 명령줄에서 실행합니다.

1. 또는 **F1** 키를 눌러 명령 팔레트를 열고, **디버그: 디버깅하지 않고 시작**을 선택합니다.
프로그램을 시작하는 방법을 설명하는 새 ``launch.json`` 파일을 만들라는 메시지가 표시될 수 있습니다.
기본 ``launch.json``은 대부분의 애플리케이션에서 제대로 작동합니다.

결과는 다음과 같아야 합니다.

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. `F5` 키를 누르기만 하면 프로그램이 빌드되고 실행됩니다!

결과는 다음과 같아야 합니다.

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

키를 누르면 프로그램이 종료됩니다.

* * *

## <a name="prepare-superposition"></a>중첩 준비

**개요** 이제 Q#에서 큐비트를 중첩된 것으로 표현하는 방법을 살펴보겠습니다.  앞에서 큐비트의 상태는 0과 1의 중첩일 수 있다고 했습니다.  `Hadamard` 연산을 사용하여 큐비트를 중첩하겠습니다. 큐비트가 두 클래식 상태 중 하나인 경우(즉, 측정에서 항상 `Zero`를 반환하거나 항상 `One`을 반환) `Hadamard` 또는 `H` 연산은 큐비트 측정 시 시간 중 50%는 `Zero`를 반환하고 시간 중 50%는 `One`을 반환하는 상태로 큐비트 상태를 전환합니다.  개념적으로 큐비트는 `Zero`와 `One`의 중간으로 생각할 수 있습니다.  이제 `TestBellState` 연산을 시뮬레이션하면 측정 후 반환된 `Zero` 및 `One`의 수가 거의 동일한 것을 볼 수 있습니다.  

먼저 큐비트를 전환하겠습니다(큐비트가 `Zero` 상태이면 `One` 상태로 전환하고 그 반대의 경우도 마찬가지). 이 작업은 `X` 연산을 수행한 후 `TestBellState`에서 측정하는 순서로 진행됩니다.

```qsharp
X(qubit);
let res = M(qubit);
```

이제 `F5` 키를 누르면 결과가 되돌려집니다.

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

그러나 지금까지 살펴본 모든 것은 클래식입니다. 양자 결과를 가져올 수 있습니다. 이전 실행의 `X` 연산을 `H` 또는 Hadamard 연산으로 바꾸기만 하면 됩니다. 큐비트를 0에서 1까지 완전히 대칭 이동하는 대신, 절반만 대칭 이동합니다. 이제 `TestBellState`에서 대체된 줄은 다음과 같습니다.

```qsharp
H(qubit);
let res = M(qubit);
```

이제 결과가 더 흥미로워집니다.

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

측정할 때마다 클래식 값을 요청하지만, 큐비트는 0에서 1 사이의 중간에 있으므로 통계적으로 0과 1을 절반씩 가져옵니다. 이를 __중첩__이라고 하며, 양자 상태에 대한 첫 번째 실제 보기를 제공합니다.

## <a name="prepare-entanglement"></a>얽힘 준비

**개요:**  이제 Q#에서 큐비트를 얽매는 방법을 살펴보겠습니다.  먼저 첫 번째 큐비트를 초기 상태로 설정한 다음, `H` 연산을 사용하여 중첩 상태로 전환합니다.  그리고 첫 번째 큐비트를 측정하기 전에, Controlled-Not을 나타내는 새로운 연산(`CNOT`)을 사용합니다.  두 큐비트에 대해 이 연산을 실행하면 그 결과로 첫 번째 큐비트가 `One`인 경우 두 번째 큐비트가 대칭 이동됩니다.  이제 두 큐비트가 서로 얽혔습니다.  첫 번째 큐비트에 대한 통계는 변경되지 않았지만(측정 후 `Zero` 또는 `One`일 확률이 50-50), 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다. `CNOT`는 두 큐비트를 얽어서 두 큐비트 중 한 큐비트에서 발생하는 모든 것이 다른 큐비트에서 발생하도록 했습니다. 반대로 측정한 경우(먼저 두 번째 큐비트를 측정한 후에 첫 번째 큐비트를 측정함)에도 동일한 상황이 발생합니다. 첫 번째 측정은 임의적이고, 두 번째 측정은 첫 번째 측정에서 발견된 모든 것과 함께 잠금 단계에 있습니다.

수행해야 할 첫 번째 작업은 `TestBellState`에서 1 대신 두 개의 큐비트를 할당하는 것입니다.

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

이렇게 하면 `TestBellState`에서 측정(`M`)하기 전에 새 연산(`CNOT`)을 추가할 수 있습니다.

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

시작할 때 항상 `Zero` 상태에 있도록 첫 번째 큐비트를 초기화하는 다른 `Set` 연산을 추가했습니다.

또한 두 번째 큐비트를 해제하기 전에 다시 설정해야 합니다.

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

이제 전체 루틴은 다음과 같습니다.

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

이 루틴을 실행하면 이전과 정확히 동일한 50-50의 결과를 얻을 수 있습니다. 그러나 관심이 있는 것은 두 번째 큐비트가 측정되는 첫 번째 큐비트에 반응하는 방법입니다. 새 버전의 `TestBellState` 연산을 사용하여 이 통계를 추가합니다.

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

새 반환 값(`agree`)은 첫 번째 큐비트의 측정값이 두 번째 큐비트의 측정값과 일치할 때마다 추적합니다. 또한 호스트 애플리케이션을 다음과 같이 적절히 업데이트해야 합니다.

#### <a name="python"></a>[Python](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

이제 실행하는 경우 매우 놀라운 상황이 발생합니다.

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

개요에서 설명했듯이, 첫 번째 큐비트에 대한 통계는 변경되지 않았지만(0 또는 1일 확률이 50-50), 이제 두 큐비트가 서로 얽혀 있으므로 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다.

축하합니다. 첫 양자 프로그램을 작성했습니다!

## <a name="whats-next"></a>다음 단계

[Grover의 검색](xref:microsoft.quantum.quickstarts.search) 자습서에서는 가장 인기 있는 양자 컴퓨팅 알고리즘 중 하나인 Grover 검색을 빌드하고 실행하는 방법을 보여 주고, 양자 컴퓨팅과 관련된 실제 문제를 해결하는 데 사용할 수 있는 Q# 프로그램의 좋은 예제를 제공합니다.  

[Quantum Development Kit 시작](xref:microsoft.quantum.welcome)에서는 Q# 및 양자 프로그래밍을 배울 수 있는 더 많은 방법을 추천해줍니다.

