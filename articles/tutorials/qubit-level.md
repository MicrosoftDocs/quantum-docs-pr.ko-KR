---
title: 에서의 비트 수준 프로그램 작성 및 시뮬레이트 Q#
description: 개별 기능 비트 수준에서 작동 하는 퀀텀 프로그램 작성 및 시뮬레이션에 대 한 단계별 자습서
author: gillenhaalb
ms.author: a-gibec
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
no-loc:
- Q#
- $$v
ms.openlocfilehash: 0dbeee8e092c830576ba8f79733035cdeeac11de
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834961"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a>자습서: Q:에서의 비트 수준 프로그램 작성 및 시뮬레이트\#

개별 ombits에서 작동 하는 기본 퀀텀 프로그램 작성 및 시뮬레이션에 대 한 퀀텀 Development Kit 자습서를 시작 합니다. 

Q#는 주로 대규모 퀀텀 프로그램을 위한 상위 수준 프로그래밍 언어로 만들어졌지만, 더 낮은 수준의 퀀텀 프로그램을 탐색 하는 데 쉽게 사용할 수 있습니다. 즉, 특정 비트를 직접 지정 합니다.
의 유연성을 Q# 통해 사용자는 이러한 추상화 수준에서 퀀텀 시스템에 접근 하는 데 사용할 수 있으며,이 자습서에서는 다양 한 기능을 제공 합니다.
특히, 많은 수의 큰 퀀텀 알고리즘에 필수적인 서브루틴 인 [퀀텀 푸리에 변환](https://en.wikipedia.org/wiki/Quantum_Fourier_transform)의 후드를 살펴보겠습니다.

퀀텀 정보 처리에 대 한이 하위 수준 보기는 시스템의 특정 비트에 대 한 게이트의 순차적 적용을 나타내는 "[퀀텀 회로](xref:microsoft.quantum.concepts.circuits)" 측면에서 설명 하는 경우가 많습니다.

따라서 순차적으로 적용 한 단일 및 다중 작업 비트 작업을 "회로 다이어그램"으로 쉽게 나타낼 수 있습니다.
이 경우 Q# 회로로 표시 되는 다음 표현을 포함 하는 전체 3 일 비트 퀀텀 푸리에 변환을 수행 하는 작업을 정의 합니다.

<br/>
<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a>전제 조건

* 원하는 언어 및 개발 환경을 사용 하 여 퀀텀 개발 키트를 [설치](xref:microsoft.quantum.install) 합니다.
* QDK가 이미 설치되어 있는 경우 최신 버전으로 [업데이트](xref:microsoft.quantum.update)해야 합니다.


## <a name="in-this-tutorial-youll-learn-how-to"></a>이 자습서에서 학습할 방법은 다음과 같습니다.

> [!div class="checklist"]
> * 퀀텀 작업 정의 Q#
> * Q#명령 프롬프트에서 또는 기존 호스트 프로그램을 사용 하 여 작업을 직접 호출 합니다.
> * 측정 출력에 대 한 정량 비트 할당에서 퀀텀 작업 시뮬레이트
> * 작업 전체에서 퀀텀 시스템의 시뮬레이션 된 wavefunction 진화 하는 방식 관찰

Microsoft의 퀀텀 개발 키트를 사용 하 여 퀀텀 프로그램을 실행 하는 작업은 일반적으로
1. 프로그램 자체는 퀀텀 프로그래밍 언어를 사용 하 여 구현 된 Q# 다음 퀀텀 컴퓨터 또는 퀀텀 시뮬레이터에서 실행 되도록 호출 됩니다. 다음으로 구성 됩니다. 
    - Q# 작업: 퀀텀 레지스터에 대해 작동 하는 서브루틴 
    - Q# 함수: 퀀텀 알고리즘 내에서 사용 되는 기존 서브루틴입니다.
2. 퀀텀 프로그램을 호출 하 고 실행 해야 하는 대상 컴퓨터를 지정 하는 데 사용 되는 진입점입니다.
    이 작업은 명령 프롬프트에서 직접 수행 하거나 Python 또는 c #과 같은 클래식 프로그래밍 언어로 작성 된 호스트 프로그램을 통해 수행할 수 있습니다.
    이 자습서에는 원하는 방법에 대 한 지침이 포함 되어 있습니다.

## <a name="allocate-qubits-and-define-quantum-operations"></a>이상 비트 할당 및 퀀텀 작업 정의

이 자습서의 첫 번째 부분에서는 작업을 정의 하 여 Q# `Perform3qubitQFT` 세 개의 성능에서 퀀텀 푸리에 변환을 수행 하는 작업을 정의 합니다. 

또한 함수를 사용 [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) 하 여 세 가지 wavefunction의 시뮬레이션 된 작업이 작업 전체에서 어떻게 진화 하는지 관찰 합니다.

첫 번째 단계에서는 Q# 프로젝트 및 파일을 만듭니다.
이에 대 한 단계는 프로그램을 호출 하는 데 사용 하는 환경에 따라 다르며, 각 [설치 가이드](xref:microsoft.quantum.install)에서 세부 정보를 찾을 수 있습니다.

파일의 구성 요소를 단계별로 안내 하지만 아래의 전체 블록으로도 코드를 사용할 수 있습니다.

### <a name="namespaces-to-access-other-no-locq-operations"></a>다른 작업에 액세스 하기 위한 네임 스페이스 Q#
이 파일 내에서 먼저 컴파일러에서 액세스할 네임 스페이스를 정의 합니다 `NamespaceQFT` .
기존 작업을 사용 하기 위해 작업을 수행 하기 위해 Q# 관련 `Microsoft.Quantum.<>` 네임 스페이스를 엽니다.

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a>인수를 사용 하 여 작업 정의 및 반환
다음으로 작업을 정의 합니다 `Perform3qubitQFT` .

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

지금은 작업에서 인수를 사용 하지 않고 아무 것---도 반환 하지 않습니다 .이 경우 `Unit` c #에서와 같은 개체를 반환 하 고 `void` Python에서 빈 튜플을 반환 한다는 것을 작성 합니다 `Tuple[()]` .
나중에이를 수정 하 여 측정 결과의 배열을 반환 하도록 지정 합니다. 여기서 point는 `Unit` 로 대체 됩니다 `Result[]` . 

### <a name="allocate-qubits-with-using"></a>에서의 비트 할당 `using`
Q#이 작업 내에서 먼저 다음 문을 사용 하 여 세 가지의 레지스터를 할당 합니다 `using` .

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

을 사용 하는 경우에는 `using` $ \ket $ 상태에서 해당 비트가 자동으로 할당 됩니다 {0} . 및를 사용 하 여이를 확인할 수 있습니다 [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) .이는 문자열과 시스템의 현재 상태를 콘솔에 출력 합니다.

> [!NOTE]
> 및 `Message(<string>)` `DumpMachine()` 함수 ( [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) 각각 및)는 콘솔에 직접 인쇄 합니다. 실제 퀀텀 계산과 마찬가지로에서는이를 Q# 통해 원하는 비트 상태에 직접 액세스할 수 없습니다.
> 그러나는 `DumpMachine` 대상 컴퓨터의 현재 상태를 인쇄 하므로 전체 상태 시뮬레이터와 함께 사용 될 때 디버깅 및 학습에 대 한 중요 한 정보를 제공할 수 있습니다.


### <a name="applying-single-qubit-and-controlled-gates"></a>단일 및 제어 되는 게이트 적용

다음으로 작업 자체를 구성 하는 게이트를 적용 합니다.
Q# 에는 네임 스페이스의 작업으로 기본 퀀텀 게이트가 이미 많이 포함 되어 [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) 있으며, 이러한 작업은 예외는 아닙니다. 

Q#물론 작업 내에서 callables을 호출 하는 문은 순차적으로 실행 됩니다.
따라서 첫 번째는 적용 되는 첫 번째 게이트가 [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard)입니다.

<br/>
<img src="../media/qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

레지스터 (예: 배열의 단일)에 작업을 적용 하려면 `Qubit` `Qubit[]` 표준 인덱스 표기법을 사용 합니다.
따라서를 [`H`](xref:microsoft.quantum.intrinsic.h) 등록의 첫 번째 비트에 적용 하면 `qs` 다음 형식이 사용 됩니다.

```qsharp
            H(qs[0]);
```

(Hadamard) 게이트를 개별의 개별 비트에 적용 하는 것 외에도 `H` QFT 회로는 주로 제어 되는 회전으로 구성 됩니다 [`R1`](xref:microsoft.quantum.intrinsic.r1) .
`R1(θ, <qubit>)`일반적으로 작업은 {0} $e ^ {i\theta} $의 회전을 $ \ket $ 구성 요소에 적용 하는 동안의 $ \ket $ 구성 요소를 변경 하지 않고 그대로 유지 합니다 {1} .

#### <a name="controlled-operations"></a>제어된 연산

Q# 를 사용 하면 하나 또는 여러 컨트롤의 컨트롤에 대 한 작업 실행이 매우 쉽습니다.
일반적으로 호출을로 호출 하 `Controlled` 고 작업 인수가 다음과 같이 변경 됩니다.

 `Op(<normal args>)` $ \to $ `Controlled Op([<control qubits>], (<normal args>))` .

컨트롤은 단일 비트 인 경우에도 배열로 제공 되어야 합니다.

이후에는 `H` 다음 게이트가 `R1` 첫 번째의 작업을 수행 하 고 두 번째/셋째로 제어 되는 게이트 임을 알 수 있습니다.

<br/>
<img src="../media/qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

다음을 사용 하 여이를 호출 합니다.

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

네임 스페이스의 함수를 사용 하 여 [`PI()`](xref:microsoft.quantum.math.pi) [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) pi 라디안 측면에서 회전을 정의 합니다.
또한 정수로 나누기는 `Double` `2.0` `2` 형식 오류를 throw 하기 때문에 (예:)로 나눕니다. 

> [!TIP]
> `R1(π/2)` 및 `R1(π/4)` 는 `S` 및 `T` 작업과 동일 합니다 (에도 해당 `Microsoft.Quantum.Intrinsic` ).


관련 `H` 작업 및 제어 된 회전을 두 번째 및 세 번째 비트에 적용 한 후:

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

회로를 완료 하려면 게이트를 적용 하기만 하면 됩니다 [`SWAP`](xref:microsoft.quantum.intrinsic.swap) .

```qsharp
            SWAP(qs[2], qs[0]);
```

이는 양자를 사용 하는 경우에 필요 합니다. 즉, 양자를 사용 하 여 서브루틴을 더 큰 알고리즘으로 원활 하 게 통합할 수 있습니다.

따라서 작업에 퀀텀 푸리에 변환의 엔터프라이즈급 비트 작업을 작성 했습니다 Q# .

<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

그러나 아직 하루에는 호출할 수 없습니다.
Microsoft는이 기능을 할당 했을 때 $ \ket $ 상태에 있었지만, {0} 대부분의 경우에는이를 발견 한 것 Q# 과 같은 방식으로 유지 해야 합니다.

### <a name="deallocate-qubits"></a>비트 할당 취소

다시 호출 [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) 하 여 사후 작업 상태를 확인 하 고, 마지막으로를 호출 하 여 작업을 완료 하기 전에 다음과 같이를 다시 호출 하 여 작업을 [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) 완료 하기 전에이를 $ \ket $로 다시 설정 합니다 {0} .

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

할당 되지 않은 모든 작업을 명시적으로 $ \ket $로 설정 해야 하는 것 {0} 은 다른 작업에서 동일한 기능을 사용 하기 시작할 때 해당 상태를 정확 하 게 알 수 있기 때문에의 기본 기능입니다 Q# (리소스 부족).
또한 시스템의 다른 모든 비트를 사용 하는 것은 아닙니다.
할당 블록의 끝에서 reset을 수행 하지 않으면 `using` 런타임 오류가 발생 합니다.

이제 전체 Q# 파일이 다음과 같이 표시 됩니다.

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


Q#파일 및 작업이 완료 되 면 퀀텀 프로그램을 호출 하 고 시뮬레이션할 준비가 된 것입니다.

## <a name="run-the-program"></a>프로그램 실행

Q#작업을 파일에 정의 했으므로 `.qs` 이제 해당 작업을 호출 하 고 반환 된 모든 기존 데이터를 관찰 해야 합니다.
지금은 반환 된 내용이 없습니다 (위에서 정의한 작업이 반환 됨 `Unit` ). 하지만 나중에 Q# 측정 결과 ()의 배열을 반환 하도록 작업을 수정 하는 경우이를 `Result[]` 해결 합니다.

프로그램을 호출 하는 데 사용 되는 환경에서 프로그램을 실행 하는 동안에는이 작업을 수행 하는 Q# 방식이 다릅니다. 따라서 Q# 응용 프로그램에서 작업 하거나 Python 또는 c #에서 호스트 프로그램을 사용 하 여 설정에 해당 하는 탭의 지침을 따르세요.

#### <a name="command-prompt"></a>[명령 프롬프트](#tab/tabid-cmdline)

Q#명령 프롬프트에서 프로그램을 실행 하려면 파일을 약간만 변경 해야 Q# 합니다.

`@EntryPoint()`작업 정의 앞의 줄에를 추가 하기만 하면 됩니다.

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

프로그램을 실행 하려면 프로젝트의 폴더에서 터미널을 열고 다음을 입력 합니다.

```dotnetcli
dotnet run
```

완료 되 면 `Message` `DumpMachine` 아래의 및 출력이 콘솔에 인쇄 됩니다.


#### <a name="python"></a>[Python](#tab/tabid-python)

Python 호스트 파일을 만듭니다 `host.py` .

호스트 파일은 다음과 같이 구성 됩니다. 
1. 먼저 모듈 `qsharp` 을 가져오고,이 모듈은 상호 운용성을 위해 모듈 로더를 등록 합니다 Q# . 
    이렇게 하면 Q# 네임 스페이스 (예: `NamespaceQFT` 파일에 정의 된 Q# )를 Python 모듈로 표시 하 여 작업을 가져올 수 있습니다. Q#
2. 그런 다음 Q# 이 경우---직접 호출 하는 작업 (이 경우)을 가져옵니다 `Perform3qubitQFT` .
    진입점을 프로그램 으로만 가져와야 Q# 합니다. _not_ 즉 `H` `R1` , 다른 작업에 의해 호출 Q# 되지만 기존 호스트에서 호출 하지 않는 및와 같은 작업은 아닙니다.
3. Q#작업 또는 함수를 시뮬레이션 하는 경우 폼을 사용 `<Q#callable>.simulate(<args>)` 하 여 `QuantumSimulator()` 대상 컴퓨터에서 실행 합니다. 

> [!NOTE]
> 예를 들어와 같이 다른 컴퓨터에서 작업을 호출 하려는 경우를 `ResourceEstimator()` 사용 `<Q#callable>.estimate_resources(<args>)` 합니다.
> 일반적으로 Q# 작업은 실행 되는 컴퓨터와는 독립적 이지만와 같은 일부 기능은 `DumpMachine` 다르게 동작할 수 있습니다.

4. 시뮬레이션을 수행할 때 작업 호출은 파일에 정의 된 대로 값을 반환 합니다 Q# .
    지금은 아무 것도 반환 되지 않지만 나중에 이러한 값을 할당 하 고 처리 하는 예제를 볼 수 있습니다.
    실습 및 완전히 고전의 결과 데이터를 사용 하 여 원하는 작업을 수행할 수 있습니다.

전체 `host.py` 파일은 다음과 같아야 합니다.

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

Python 파일을 실행 하 고 콘솔에 인쇄 하 여 `Message` 아래와 출력을 확인 해야 합니다 `DumpMachine` . 


#### <a name="c"></a>[C#](#tab/tabid-csharp)

[설치 가이드](xref:microsoft.quantum.install.cs)에 나와 있는 것과 동일한 지침에 따라 c # 호스트 파일을 만들고 이름을로 바꿉니다 `host.cs` .

C # 호스트는 네 부분으로 구성 됩니다.
1. 양자 시뮬레이터를 생성합니다.
    아래 코드에서 변수입니다 `qsim` .
2. 양자 알고리즘에 필요한 인수를 계산합니다.
    이 예제에는 없음이 있습니다.
3. 양자 알고리즘을 실행합니다. 
    각 Q# 작업은 동일한 이름의 c # 클래스를 생성 합니다. 
    이 클래스에는 `Run` **비동기**작업을 실행 하는 메서드가 있습니다.
    실제 하드웨어에서 실행 하는 것은 비동기식으로 실행 되기 때문입니다. 
    메서드가 비동기 이기 때문에 `Run` 메서드를 호출 합니다 `Wait()` .이 메서드는 작업이 완료 될 때까지 실행을 차단 하 고 결과를 동기적으로 반환 합니다. 
4. 작업의 반환 된 결과를 처리 합니다.
    지금은 작업에서 아무 것도 반환 하지 않습니다.


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
응용 프로그램을 실행 하면 출력이 아래와 일치 해야 합니다.
키를 누르면 프로그램이 종료됩니다.
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

전체 상태 시뮬레이터에서 호출 될 때는 `DumpMachine()` 퀀텀 상태 wavefunction의 다양 한 표현을 제공 합니다. $N $-hbit 시스템의 가능한 상태는 $2 ^ n $ 계산 기준 상태로 표시 될 수 있으며 각각은 해당 하는 복잡 한 계수 (진폭 및 단계)를 포함 합니다.
계산 기준 상태는 가능한 모든 이진 문자열 길이 $n $---즉, \ket $ 및 $ \ket $ 및 $ $의 가능한 모든 조합에 해당 합니다 {0} {1} . 여기서 각 이진 숫자는 개별 비트에 해당 합니다.

첫 번째 행은 중요 한 순서 대로 해당 하는의 Id를 사용 하 여 주석을 제공 합니다.
`2`"가장 중요 한" 것은 단지 기본 상태 vector $ \ket{i} $의 이진 표현에서, 고 비트의 상태는 `2` 맨 왼쪽 숫자에 해당 하는 것을 의미 합니다. 예를 들어 $ \ket {6} = \ket {110} $은 $ `2` `1` \ket $의 $ \ket $ 및의 두 가지로 구성 {1} `0` {0} 됩니다.


나머지 행은 데카르트 및 극좌표 형식의 기본 상태 vector $ \ket{i} $를 측정 하는 확률 진폭을 설명 합니다.
입력 상태 $ \ket $의 첫 번째 행에 대해 자세히 설명 합니다 {000} .
* **`|0>:`** 이 행은 `0` 계산 기준 상태에 해당 합니다 (초기 상태 사후 할당이 $ \ket $로 지정 된 {000} 경우이 시점에서 확률 진폭의 유일한 상태가 됨).
* **`1.000000 +  0.000000 i`**: 데카르트 형식의 확률 진폭입니다.
* **` == `**: `equal` 부호는 두 동등한 표현을 구분 합니다.
* **`********************`**: 크기의 그래픽 표현으로,의 수는 `*` 이 상태 벡터를 측정할 확률에 비례 합니다. 
* **`[ 1.000000 ]`**: 크기의 숫자 값입니다.
* **`    ---`**: 진폭의 단계를 그래픽으로 표현한 것입니다.
* **`[ 0.0000 rad ]`**: 단계의 숫자 값 (라디안 단위)입니다.

크기와 단계가 모두 그래픽 표현으로 표시 됩니다. 크기 표현은 간단 합니다. 즉, 막대를 표시 하 `*` 고 확률이 높을수록 막대가 커집니다. 단계는 [테스트 및 디버깅:](xref:microsoft.quantum.guide.testingdebugging#dump-functions) 각도 범위를 기준으로 가능한 기호 표현의 덤프 함수를 참조 하세요.


따라서 인쇄 된 출력은 프로그래밍 된 게이트가

$ $ \ket{\psi} \_ {초기} = \ket {000} $ $

을 

$ $ \begin{align} \ket{\psi} \_ {final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $

이는 3-이상 비트 푸리에 변환의 동작입니다. 

다른 입력 상태가 영향을 받는 방법에 대 한 자세한 내용을 보려면 변형 전에 원하는 비트 작업을 적용 하는 것이 좋습니다.

## <a name="adding-measurements"></a>측정값 추가

불행 하 게도 퀀텀 메커니즘을 cornerstone 실제 퀀텀 시스템은 이러한 기능을 가질 수 없다는 것을 알 수 `DumpMachine` 있습니다. 대신 일반적으로 전체 퀀텀 상태를 제공 하는 데 실패할 뿐만 아니라 시스템 자체를 크게 변경할 수 있는 측정을 통해 정보를 추출 해야 합니다.
다양 한 종류의 퀀텀 측정이 있지만 가장 기본적인: projective 측정에 중점을 두고 있습니다.
지정 된 기준 (예: 계산 기준 $ \{ \ket {0} , \ket $)을 기준으로 하는 경우에는 {1} \} 두 값 사이에 있는 모든 superposition를 소멸---측정 된 기준에 따른 비트 상태를 예측 합니다.

프로그램 내에서 측정을 구현 하기 위해 Q# `M` 형식을 반환 하는 작업 (의 경우)을 사용 합니다 `Microsoft.Quantum.Intrinsic` `Result` .

첫째, `Perform3QubitQFT` 대신 측정 결과 배열을 반환 하도록 작업을 수정 `Result[]` `Unit` 합니다.

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a>배열 정의 및 초기화 `Result[]`

이 경우에는 (즉, 문 앞에 있는 `using` ),이 세 번째 길이의 배열을 선언 하 고 바인딩합니다. `Result` 

```qsharp
        mutable resultArray = new Result[3];
```

`mutable`앞 키워드를 `resultArray` 사용 하면---코드에서 나중에 (예: 측정 결과를 추가할 때) 변수를 다시 바인딩할 수 있습니다.

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a>루프에서 측정값을 수행 `for` 하 고 배열에 결과를 추가 합니다.

블록 내의 푸리에 변환 작업 후에 `using` 다음 코드를 삽입 합니다.

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
[`IndexRange`](xref:microsoft.quantum.arrays.indexrange)배열에 대해 호출 되는 함수 (예: 값의 배열)는 `qs` 배열의 인덱스에 대해 범위를 반환 합니다. 여기서 `for` 는 문을 사용 하 여 각 비트를 순차적으로 측정 하기 위해 루프에서 사용 `M(qs[i])` 합니다.
그러면 각 측정 된 `Result` 형식 ( `Zero` 또는 `One` )이 `resultArray` 업데이트 및 재할당 문으로의 해당 인덱스 위치에 추가 됩니다.

> [!NOTE]
> 이 문의 구문은에 고유 Q# 하지만 `resultArray[i] <- M(qs[i])` F # 및 R과 같은 다른 언어에서 보이는 유사한 변수 재할당에 해당 합니다.

키워드는를 `set` 사용 하 여 바인딩된 변수를 다시 할당 하는 데 항상 사용 됩니다 `mutable` .

#### <a name="return-resultarray"></a>돌려 `resultArray`

3 개의 모든 비트를 측정 하 고 결과를에 추가 하 여 `resultArray` 이전 처럼 이제는이를 다시 설정 하 고 할당을 취소 해도 됩니다.
`using`블록을 닫은 후 삽입 합니다.

```qsharp
        return resultArray;
```
궁극적으로 작업의 출력을 반환 합니다. 

### <a name="understanding-the-effects-of-measurement"></a>측정 효과 이해

`DumpMachine`측정 전후에 상태를 출력 하도록 함수의 배치를 변경해 보겠습니다.
최종 작업 코드는 다음과 같습니다. 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

명령 프롬프트에서 작업 하는 경우 반환 된 배열은 단순히 실행이 끝날 때 콘솔에 직접 표시 됩니다.
그렇지 않으면 반환 된 배열을 처리 하도록 호스트 프로그램을 업데이트 합니다.

#### <a name="command-prompt"></a>[명령 프롬프트](#tab/tabid-cmdline)

콘솔에 출력 되는 반환 된 배열을 보다 잘 이해 하기 위해 `Message` 문 바로 앞에 다른 파일을 추가할 수 있습니다 Q# `return` .

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

프로젝트를 실행 하면 출력이 다음과 같이 표시 됩니다.

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[Python](#tab/tabid-python)

Python 프로그램을 다음으로 업데이트 합니다.

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

파일을 실행 하면 출력이 다음과 같이 표시 됩니다.

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

이제 작업에서 결과를 반환 했으므로 메서드 호출을 `Wait()` 속성 인출으로 바꿉니다 `Result` . 이는 앞에서 설명한 것과 동일한 synchronicity을 계속 수행 하 고이 값을 변수에 직접 바인딩할 수 있습니다 `measurementResult` .

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

프로젝트를 실행 하면 출력이 다음과 같이 표시 됩니다.

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

이 출력은 몇 가지 다른 항목을 보여 줍니다.
1. 반환 된 결과를 사전 측정 결과와 비교 하는 `DumpMachine` 것은 기준 상태에 대해 QFT superposition를 명확 하 게 설명 _하지_ 않습니다.
    측정은 시스템의 wavefunction에서 해당 상태의 진폭에 의해 결정 되는 확률을 사용 하 여 단일 기준 상태만 반환 합니다.
2. 사후 측정에서 측정값은 `DumpMachine` 상태 자체를 _변경_ 하 여 초기 superposition 기준 상태를 측정 된 값에 해당 하는 단일 기준 상태로 프로젝션 합니다.

이 작업을 여러 번 반복 하는 경우 결과 통계는 각 샷의 무작위 결과를 제공 하는 QFT 상태의 동일 하 게 가중치가 적용 된 superposition을 보여 주기 시작 합니다.
_그러나_비효율적이 고 여전히 아직까지 완벽 하는 것 외에도,이 경우에는 그 사이에 상대적인 단계가 아니라 전용 상태의 상대적 amplitudes 재현할 수 있습니다.
후자는이 예에서는 문제가 되지 않지만 $ \ket $ 보다 QFT에 더 복잡 한 입력이 지정 된 경우에는 상대 단계가 표시 됩니다 {000} .

#### <a name="partial-measurements"></a>부분 측정 
레지스터의 일부를 측정 하 여 시스템의 상태에 영향을 줄 수 있는 방법을 살펴보려면 다음을 루프 내부에 추가 해 보세요 `for` .
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

이 함수에 액세스 하려면 다음을 추가 해야 합니다. `IntAsString` 
```qsharp
    open Microsoft.Quantum.Convert;
```
나머지 네임 스페이스 `open` 문을 사용 합니다.

결과 출력에서 각 고가 측정 될 때 하위 공간에 대 한 점진적 프로젝션을 볼 수 있습니다.


## <a name="use-the-no-locq-libraries"></a>라이브러리 사용 Q#
소개 부분에서 언급 했 듯이, 대부분의 Q# 능력은 개별 신경 쓰지를 처리 하는 것이 가능 하다는 사실에 있습니다.
실제로, 적용 가능한 모든 퀀텀 프로그램을 개발 하려는 경우 특정 순환의 전후에 작업이 발생 하는지 걱정 해도 `H` 속도가 저하 될 수 있습니다. 

라이브러리에는 Q# [qft](xref:microsoft.quantum.canon.qft) 연산이 포함 되어 있으며,이 작업은 원하는 수의 다양 한 비트에 대해 간단 하 게 적용 및 적용할 수 있습니다.
이 작업을 수행 하려면의 내용이 동일한 파일에 새 작업을 정의 합니다 .이 작업은 첫 번째에서 Q# `Perform3QubitQFT` 로 대체 되는 모든 항목을 `H` `SWAP` 두 개의 간단한 줄로 바꿉니다.
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
첫 번째 줄에서는 [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) `qs` [qft](xref:microsoft.quantum.canon.qft) 작업에서 인수로 사용 되는,의 할당 된 배열의 식을 만듭니다.
이는 레지스터의 고 비트의 인덱스 순서에 해당 합니다.

이러한 작업에 액세스 하려면 `open` 파일의 시작 부분에 해당 네임 스페이스에 대 한 문을 추가 합니다 Q# .
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

이제 호스트 프로그램을 조정 하 여 새 작업의 이름 (예:)을 호출 하 `PerformIntrinsicQFT` 고 그럼를 제공 합니다.

라이브러리 작업 사용에 대 한 실제 혜택을 확인 하려면 Q# 다음과 같은 값을 변경 하는 것이 좋습니다 `3` .
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
따라서 `H` 각 이상에서 새로운 작업 및 회전에 대해 걱정할 필요 없이 지정 된 수의 수 만큼 적절 한 QFT를 적용할 수 있습니다.

실제 퀀텀 하드웨어로 전환 하는 이유를 정확 하 게---하는 것 처럼, 퀀텀 시뮬레이터를 실행 하는 데 많은 시간이 소요 됩니다.













