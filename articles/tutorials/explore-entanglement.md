---
title: 되거나 얽 히를 사용 하 여 탐색 Q#
description: 에서 퀀텀 프로그램을 작성 하는 방법에 대해 알아봅니다 Q# . QDK(Quantum Development Kit)를 사용하여 Bell State 애플리케이션을 개발합니다.
author: geduardo
ms.author: v-edsanc
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
no-loc:
- Q#
- $$v
ms.openlocfilehash: 7a1a49e18ac9330ca6e3cc89b3e58c96eccb91db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691661"
---
# <a name="tutorial-explore-entanglement-with-q"></a>자습서: Q\#을 사용한 얽힘 살펴보기

이 자습서에서는 Q# 다양 한 비트를 조작 하 고 측정 하는 프로그램을 작성 하 고 superposition 및 되거나 얽 히의 효과를 보여 줍니다.

양자 얽힘을 보여주는 벨이라는 애플리케이션을 작성합니다.
벨이라는 이름은 가장 간단한 중첩과 양자 얽힘의 예를 표현하는 데 사용되는 두 큐비트의 특정 양자 상태를 의미하는 벨 상태에서 따온 것입니다.

## <a name="pre-requisites"></a>필수 구성 요소

코딩을 시작할 준비가 되면 계속하기 전에 다음 단계를 수행합니다. 

* 원하는 언어 및 개발 환경을 사용 하 여 퀀텀 개발 키트를 [설치](xref:microsoft.quantum.install) 합니다.
* QDK가 이미 설치되어 있는 경우 최신 버전으로 [업데이트](xref:microsoft.quantum.update)해야 합니다.

QDK를 설치 하지 않고도 설명을 따라 수행 하 고, Q# 프로그래밍 언어의 개요와 퀀텀 컴퓨팅의 첫 번째 개념을 검토할 수도 있습니다.

## <a name="in-this-tutorial-youll-learn-how-to"></a>이 자습서에서 학습할 방법은 다음과 같습니다.

> [!div class="checklist"]
> * Q에서 작업 만들기 및 결합\#
> * Superposition, entangle에 원하는 비트를 배치 하 고 측정 하는 작업을 만듭니다.
> * 시뮬레이터에서 프로그램이 실행 되는 퀀텀 되거나 얽 히을 보여 줍니다 Q# . 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a>QDK 동작 시연

클래식 비트는 0 또는 1 같은 단일 이진 값을 보유하는 반면, [큐비](xref:microsoft.quantum.glossary#qubit) 상태는 0과 1의 **중첩** 에 있을 수 있습니다.  개념적으로,의 상태는 추상 공간 (벡터가 라고도 함)의 방향으로 간주할 수 있습니다.  이 경우 가능한 모든 방향이 있을 수 있습니다. 두 **클래식 상태** 는 두 방향입니다. 즉, 0을 측정할 확률이 100%이고, 1을 측정할 확률이 100%입니다.

측정 작업은 이진 결과를 생성하고 큐비트 상태를 변경합니다.
측정은 0 또는 1의 이진 값을 생성 합니다.  큐비트는 중첩(모든 방향)에서 클래식 상태 중 하나로 변경됩니다.  그 후 개입 작업 없이 동일한 측정을 반복하여 동일한 이진 결과를 생성합니다.  

여러 큐비트가 서로 [**얽힐**](xref:microsoft.quantum.glossary#entanglement) 수 있습니다.  얽힌 큐비트 하나를 측정하면 다른 큐비트의 상태 정보도 업데이트됩니다.

이제에서이 동작을 표현 하는 방법을 보여 드릴 준비가 되었습니다 Q# .  가능한 가장 간단한 프로그램으로 시작하여 양자 중첩 및 양자 얽힘을 보여주는 프로그램을 빌드합니다.

## <a name="creating-a-no-locq-project"></a>프로젝트 만들기 Q#

가장 먼저 해야 할 일은 새 프로젝트를 만드는 것입니다 Q# . 이 자습서에서는 VS Code를 사용 하는 [ Q# 응용 프로그램](xref:microsoft.quantum.install.standalone)을 기반으로 환경을 사용 합니다.

새 프로젝트를 만들려면 VS Code에서 다음을 수행 합니다. 

1. **보기** -> **명령 팔레트** 를 클릭하고 **Q#: 새 프로젝트 만들기** 를 선택합니다.
2. **Standalone console application** (독립 실행형 콘솔 애플리케이션)을 클릭합니다.
3. 프로젝트를 저장할 위치로 이동하여 **프로젝트 만들기** 를 클릭합니다.
4. 프로젝트가 만들어지면 오른쪽 아래에서 **Open new project...** (새 프로젝트 열기)를 클릭합니다.

이 경우 프로젝트를 호출 했습니다 `Bell` . 그러면 `Bell.csproj` `Program.qs` 응용 프로그램을 작성 하는 데 사용할 응용 프로그램의 템플릿인, 프로젝트 파일 및 라는 두 개의 파일이 생성 Q# 됩니다. 의 내용은 `Program.qs` 다음과 같아야 합니다.

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a>Q \# 응용 프로그램 작성
 
Microsoft의 목표는 특정 퀀텀 상태에서 두 개의 작업을 준비 하는 것입니다 .를 사용 하 여이 작업을 수행 하 여 Q# 상태를 변경 하 고 superposition 및 되거나 얽 히의 효과를 보여 주는 방법을 보여 줍니다. 여기서는이를 구성 하 여 몇 비트 상태, 작업 및 측정을 소개 합니다.

### <a name="initialize-qubit-using-measurement"></a>측정을 사용 하 여 비트를 초기화 합니다.

아래의 첫 번째 코드 조각에서는에서 원하는 비트를 사용 하는 방법을 보여 줍니다 Q# .  여기서는 두 가지 작업을 소개 하 고,이를 통해 [`M`](xref:Microsoft.Quantum.Intrinsic.m) [`X`](xref:Microsoft.Quantum.Intrinsic.X) 원하는 비트의 상태를 변환 합니다. 이 코드 조각에서 `SetQubitState` 연산은 큐비트를 매개 변수로 사용하고 또 다른 매개 변수 `desired`를 사용하여 우리가 원하는 큐비트 상태를 나타내는 것으로 정의됩니다.  `SetQubitState` 연산은 `M` 연산을 사용하여 큐비트를 측정합니다.  에서 Q# ,의 비트 측정은 항상 또는를 반환 합니다 `Zero` `One` .  측정값이 원하는 값과 일치 하지 않는 값을 반환 하는 경우에는 해당 값을 `SetQubitState` "대칭 이동" 합니다. 즉, `X` 작업을 실행 합니다 .이 작업은이를 반환 하는 측정값의 확률을 반환 하는 새 상태로의 값을 변경 하는 작업을 실행 `Zero` `One` 합니다. 이러한 방식으로 `SetQubitState` 는 항상 대상의를 원하는 상태로 설정 합니다.

의 내용을 `Program.qs` 다음 코드로 바꿉니다.


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

이제 이 연산을 호출하여 큐비트를 클래식 상태로 설정하면 항상 `Zero`를 반환하거나 항상 `One`을 반환할 수 있습니다.
`Zero` 및 `One`은 큐비트 측정에서 가능한 두 가지 결과를 나타내는 상수입니다.

`SetQubitState` 연산은 큐비트를 측정합니다. 원하는 비트가 원하는 상태에 있는 경우에 `SetQubitState` 만 그대로 둡니다. 그렇지 않으면 작업을 실행 하 여 `X` 원하는 상태로 변경 합니다.

#### <a name="about-no-locq-operations"></a>Q#작업 정보

Q#작업은 퀀텀 서브루틴입니다. 즉, 다른 퀀텀 작업에 대 한 호출을 포함 하는 호출 가능 루틴입니다.

연산에 대한 인수는 괄호로 묶인 튜플로 지정됩니다.

연산의 반환 형식은 콜론 뒤에 지정됩니다. 이 경우 `SetQubitState` 작업은 반환 형식을 포함 하지 않으므로 반환 되는 것으로 표시 됩니다 `Unit` . 이는 c #의와 거의 유사한 F #의에 해당 하는 것입니다 .이는 Q# `unit` `void` 형식 힌트로 표현 되는 Python의 빈 튜플입니다 `()` `Tuple[()]` .

첫 번째 작업에서 두 개의 퀀텀 작업을 사용 했습니다 Q# .

* [`M`](xref:Microsoft.Quantum.Intrinsic.m)작업으로,이 작업은의 상태를 측정 합니다.
* [`X`](xref:Microsoft.Quantum.Intrinsic.X)작업은이 작업을 수행 합니다.

양자 연산은 큐비트의 상태를 변환합니다. 가끔 사람들은 클래식 논리 게이트와 비슷하게, 연산 대신 양자 게이트에 대해 이야기합니다. 그 기원은 알고리즘이 이론적 아이디어에 불과했고 클래식 컴퓨팅의 회로 다이어그램과 유사한 다이어그램으로 시각화되던 양자 컴퓨팅 초기 시대입니다.

### <a name="counting-measurement-outcomes"></a>측정 결과 계산

`SetQubitState` 연산의 효과를 보여주기 위해 `TestBellState` 연산이 추가됩니다. 이 연산은 `Zero` 또는 `One`을 입력으로 취하며, 이 입력을 사용하여 `SetQubitState` 연산을 몇 차례 호출하고, 큐비트 측정에서 `Zero`가 반환된 횟수와 `One`이 반환된 횟수를 집계합니다. 물론 `TestBellState` 연산의 첫 번째 시뮬레이션 출력에서는 `Zero`를 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `Zero`를 반환하고, `One`을 사용하여 매개 변수 입력으로 설정된 모든 큐비트 측정에서 `One`을 반환할 것으로 예상됩니다. 또한에 코드를 추가 하 여 `TestBellState` superposition 및 되거나 얽 히를 보여 줍니다.

`SetQubitState` 연산이 끝난 후 다음 연산을 네임스페이스 내의 `Program.qs` 파일에 추가합니다.

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
`return`() 함수 ()를 사용 하 여 콘솔에 설명 메시지를 인쇄 하기 위해 앞에 줄을 추가 했습니다 ( `Message` ).

이 연산(`TestBellState`)은 `count` 반복에 대해 루프를 실행하고, 큐비트에 지정된 `initial` 값을 설정한 다음, 결과를 측정합니다(`M`). 측정한 0과 1의 개수에 대한 통계를 수집하여 호출자에게 반환합니다. 다른 필요한 연산을 수행합니다. 다른 사용자가 알려진 상태에서 이 큐비트를 할당할 수 있도록 반환하기 전에 해당 큐비트를 알려진 상태(`Zero`)로 다시 설정합니다. 이는 `using` 문에 필요합니다.

#### <a name="about-variables-in-q"></a>Q의 변수 정보\#

기본적으로의 변수 Q# 는 변경할 수 없으며, 바인딩된 후에는 해당 값이 변경 되지 않을 수 있습니다. `let` 키워드는 변경할 수 없는 변수의 바인딩을 나타내는 데 사용됩니다. 연산 인수는 항상 변경할 수 없습니다.

예제의 `numOnes`와 같이 값이 변경될 수 있는 변수가 필요한 경우 `mutable` 키워드를 사용하여 해당 변수를 선언할 수 있습니다. 변경할 수 있는 변수의 값은 `set` 문을 사용하여 변경할 수 있습니다.

두 경우 모두에서 변수 형식은 컴파일러를 통해 유추됩니다. Q# 변수에는 형식 주석이 필요 하지 않습니다.

#### <a name="about-using-statements-in-q"></a>`using`Q의 문 정보\#

`using`문은에도 특수 Q# 합니다. 코드 블록에서 사용할 큐비트를 할당하는 데 사용됩니다. 에서는 Q# 복잡 한 알고리즘의 전체 수명 동안 유지 되는 고정 리소스 대신 모든 모든 비트를 동적으로 할당 하 고 해제 합니다. `using` 문은 시작 부분에서 큐비트 세트를 할당하고, 블록의 끝에서 해당 큐비트를 해제합니다.

## <a name="run-the-code-from-the-command-prompt"></a>명령 프롬프트에서 코드를 실행 합니다.

코드를 실행 하기 위해 명령을 제공할 때 실행할 수 있는 호출할 수 *있는* 컴파일러에 지시 해야 합니다 `dotnet run` . 이 Q# 작업은 호출 가능한 바로 앞에를 사용 하 여 줄을 추가 하 여 파일을 간단히 변경 하는 방식으로 수행 됩니다 `@EntryPoint()` `TestBellState` .이 경우에는 작업을 수행 합니다. 전체 코드는 다음과 같아야 합니다.

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

프로그램을 실행 하려면 `count` `initial` 명령 프롬프트에서 및 인수를 지정 해야 합니다. 예를 들어 및을 선택 하겠습니다 `count = 1000` `initial = One` . 다음 명령을 입력합니다.

```dotnetcli
dotnet run --count 1000 --initial One
```

다음 출력을 관찰 해야 합니다.

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

로 시도 하 `initial = Zero` 는 경우 다음 사항을 확인 해야 합니다.

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a>중첩 준비

이제를 사용 하 Q# 여 superposition에를 배치 하는 방법을 살펴보겠습니다.  앞에서 큐비트의 상태는 0과 1의 중첩일 수 있다고 했습니다.  `Hadamard` 연산을 사용하여 큐비트를 중첩하겠습니다. 큐비트가 두 클래식 상태 중 하나인 경우(즉, 측정에서 항상 `Zero`를 반환하거나 항상 `One`을 반환) `Hadamard` 또는 `H` 연산은 큐비트 측정 시 시간 중 50%는 `Zero`를 반환하고 시간 중 50%는 `One`을 반환하는 상태로 큐비트 상태를 전환합니다.  개념적으로 큐비트는 `Zero`와 `One`의 중간으로 생각할 수 있습니다.  이제 `TestBellState` 연산을 시뮬레이션하면 측정 후 반환된 `Zero` 및 `One`의 수가 거의 동일한 것을 볼 수 있습니다.  

### <a name="x-flips-qubit-state"></a>`X` 가는 비트 상태를 대칭 이동 합니다.

먼저,이를 전환 하려고 합니다. 여기서는 해당 하는 비트를 전환 하려고 `Zero` `One` 합니다. 이 작업은 `X` 연산을 수행한 후 `TestBellState`에서 측정하는 순서로 진행됩니다.

```qsharp
X(qubit);
let res = M(qubit);
```

이제 결과가 반전 됩니다.

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

이제는 이상 비트의 퀀텀 속성을 살펴보겠습니다.

### <a name="h-prepares-superposition"></a>`H` superposition 준비

이전 실행의 `X` 연산을 `H` 또는 Hadamard 연산으로 바꾸기만 하면 됩니다. 큐비트를 0에서 1까지 완전히 대칭 이동하는 대신, 절반만 대칭 이동합니다. 이제 `TestBellState`에서 대체된 줄은 다음과 같습니다.

```qsharp
H(qubit);
let res = M(qubit);
```

이제 결과가 더 흥미로워집니다.

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

측정할 때마다 클래식 값을 요청하지만, 큐비트는 0에서 1 사이의 중간에 있으므로 통계적으로 0과 1을 절반씩 가져옵니다.
이를 **중첩** 이라고 하며, 양자 상태에 대한 첫 번째 실제 보기를 제공합니다.

## <a name="prepare-entanglement"></a>얽힘 준비

이제를 entangle로 표시 하는 방법을 살펴보겠습니다 Q# .
먼저 첫 번째 큐비트를 초기 상태로 설정한 다음, `H` 연산을 사용하여 중첩 상태로 전환합니다.  그런 다음, 첫 번째 비트를 측정 하기 전에 `CNOT` *제어 되지 않음* 을 나타내는 새 작업 ()을 사용 합니다.  두 개의 비트에 대해이 작업을 실행 한 결과는 첫 번째 비트를 인 경우 두 번째 비트를 대칭 이동 하는 것입니다 `One` .  이제 두 큐비트가 서로 얽혔습니다.  첫 번째 큐비트에 대한 통계는 변경되지 않았지만(측정 후 `Zero` 또는 `One`일 확률이 50-50), 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다. `CNOT`는 두 큐비트를 얽어서 두 큐비트 중 한 큐비트에서 발생하는 모든 것이 다른 큐비트에서 발생하도록 했습니다. 반대로 측정한 경우(먼저 두 번째 큐비트를 측정한 후에 첫 번째 큐비트를 측정함)에도 동일한 상황이 발생합니다. 첫 번째 측정은 임의적이고, 두 번째 측정은 첫 번째 측정에서 발견된 모든 것과 함께 잠금 단계에 있습니다.

가장 먼저 해야 할 일은에서 하나 대신 두 개의 두 비트를 할당 하는 것입니다 `TestBellState` .

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

이렇게 하면 `TestBellState`에서 측정(`M`)하기 전에 새 연산(`CNOT`)을 추가할 수 있습니다.

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

시작할 때 항상 `Zero` 상태에 있도록 첫 번째 큐비트를 초기화하는 다른 `SetQubitState` 연산을 추가했습니다.

또한 두 번째 큐비트를 해제하기 전에 다시 설정해야 합니다.

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

이제 전체 루틴은 다음과 같습니다.

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
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
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

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
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

새 반환 값(`agree`)은 첫 번째 큐비트의 측정값이 두 번째 큐비트의 측정값과 일치할 때마다 추적합니다.

가져오는 코드를 실행 합니다.

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

개요에서 설명했듯이, 첫 번째 큐비트에 대한 통계는 변경되지 않았지만(0 또는 1일 확률이 50-50), 이제 두 큐비트가 서로 얽혀 있으므로 이제 두 번째 큐비트의 측정 결과는 첫 번째 큐비트의 측정 결과와 __항상__ 동일합니다.

## <a name="next-steps"></a>다음 단계

자습서 [Grover의 검색](xref:microsoft.quantum.quickstarts.search) 에서는 가장 인기 있는 퀀텀 컴퓨팅 알고리즘 중 하나인 Grover 검색을 빌드 및 실행 하는 방법을 보여 주고, Q# 퀀텀 컴퓨팅의 실제 문제를 해결 하는 데 사용할 수 있는 프로그램의 좋은 예를 제공 합니다.  

[퀀텀 개발 키트를 시작](xref:microsoft.quantum.welcome) 하 여 배우 프로그래밍에 대 한 추가 방법을 권장 Q# 합니다.
