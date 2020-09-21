---
title: 프로그램을 실행 하는 방법 Q#
description: 프로그램을 실행 하는 다양 한 방법에 대 한 개요입니다 Q# . 명령 프롬프트에서 Q# jupyter 노트북 및 Python 또는 .net 언어의 클래식 호스트 프로그램에서.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: f24c608ffc6522cb50f512de1a02b3db4b290e83
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759819"
---
# <a name="ways-to-run-a-no-locq-program"></a>프로그램을 실행 하는 방법 Q#

퀀텀 개발 키트의 가장 큰 장점 중 하나는 플랫폼 및 개발 환경에서의 유연성입니다.
그러나이는 새로운 Q# 사용자가 [설치 가이드](xref:microsoft.quantum.install)에 있는 다양 한 옵션을 사용 하 여 혼동 하거나 부담 하지 않을 수도 있음을 의미 합니다.
이 페이지에서는 프로그램이 실행 될 때 발생 하는 상황을 설명 Q# 하 고 사용자가 수행할 수 있는 여러 가지 방법을 비교 합니다.

주요 차이점은 다음을 Q# 실행할 수 있다는 것입니다.
- 독립 실행형 응용 프로그램으로 서, Q# 가 관련 된 유일한 언어 이며 프로그램이 직접 호출 됩니다. 두 메서드는 실제로이 범주에 속합니다.
  - 명령줄 인터페이스
  - Q# Jupyter 노트북
- Python 또는 .NET 언어 (예: c # 또는 F #)로 작성 된 추가 *호스트 프로그램*을 사용 하 여 프로그램을 호출 하 고 반환 된 결과를 추가로 처리할 수 있습니다.

이러한 프로세스와 해당 차이점을 가장 잘 이해 하려면 간단한 프로그램을 고려 하 여 Q# 실행 하는 방법을 비교 합니다.

## <a name="basic-no-locq-program"></a>기본 Q# 프로그램

기본 퀀텀 프로그램은 $ \ket {0} $ 및 $ \ket $ 상태를 측정 하 고이를 측정 하 고 결과를 반환 하는 것으로 구성 되어 있을 수 있습니다 {1} .이는 확률이 동일한 두 상태 중 하나에 임의로 superposition.
실제로이 프로세스는 [퀀텀 난수 생성기](xref:microsoft.quantum.quickstarts.qrng) 빠른 시작의 핵심에 있습니다.

에서 Q# 이 작업은 다음 코드에 의해 수행 됩니다.

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

그러나이 코드는에서 실행할 수 없습니다 Q# .
이렇게 하려면 작업 본문을 구성 해야 합니다 .이 [작업](xref:microsoft.quantum.guide.basics#q-operations-and-functions)은 직접 또는 다른 작업을 통해---호출 될 때 실행 됩니다. 따라서 다음 형식의 작업을 작성할 수 있습니다.
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
입력을 `MeasureSuperposition` 사용 하지 않고 [Result](xref:microsoft.quantum.guide.types)형식의 값을 반환 하는 작업을 정의 했습니다.

이 페이지의 예제는 작업 으로만 구성 되지만 Q# *operations*설명 하는 모든 개념은 함수에 동일 하 게 관련 Q# *functions*되어 있으므로 *callables*으로 통칭 됩니다. 이러한 차이점은 [ Q# 작업 및 함수](xref:microsoft.quantum.guide.basics#q-operations-and-functions)에 대 한 기본 사항 및 [작업 및 함수](xref:microsoft.quantum.guide.operationsfunctions)에 설명 되어 있습니다.

### <a name="callable-defined-in-a-no-locq-file"></a>파일에 정의 된 호출 가능 Q#

호출 가능 하 고에서 실행 되는 것은 정확 합니다 Q# .
그러나 전체 파일을 구성 하기 위해 몇 가지 추가 항목이 필요 `*.qs` Q# 합니다.

모든 Q# 형식 및 callables (정의 하는 모든 형식 및 해당 언어의 내장 함수)은 네임 스페이스 내에서 정의 됩니다 .이 *네임 스페이스*는 각 이름에 대해 참조할 수 있는 전체 이름을 제공 합니다.

예를 들어 [`H`](xref:microsoft.quantum.intrinsic.h) 및 [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) 작업은 [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) 및 [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) 네임 스페이스 ( [ Q# 표준 라이브러리](xref:microsoft.quantum.qsharplibintro)의 일부)에 있습니다.
따라서 항상 *전체* 이름 및를 통해 호출할 수 `Microsoft.Quantum.Intrinsic.H(<qubit>)` `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` 있지만 항상이 작업을 수행 하면 매우 복잡 한 코드를 사용할 수 있습니다.

대신 `open` 위의 작업 본문에서 수행한 것 처럼 문이 보다 간결한 줄임으로 참조 될 수 있도록 합니다.
Q#따라서 작업을 포함 하는 전체 파일은 고유한 네임 스페이스를 정의 하 고 작업에서 사용 하는 callables에 대 한 네임 스페이스를 연 다음 작업을 수행 하는 것으로 구성 됩니다.

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> 열린 경우에도 네임 스페이스를 *별칭* 으로 지정할 수 있으며,이는 두 네임 스페이스의 호출 가능/형식 이름이 충돌할 경우 유용할 수 있습니다.
> 예를 들어, 위의을 대신 사용 하 고를 통해를 호출할 수 있습니다 `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` `H` `NamespaceWithH.H(<qubit>)` .

> [!NOTE]
> 이에 대 한 한 가지 예외는 [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) 항상 자동으로 열리는 네임 스페이스입니다.
> 따라서와 같은 callables은 [`Length`](xref:microsoft.quantum.core.length) 항상 직접 사용할 수 있습니다.

### <a name="execution-on-target-machines"></a>대상 컴퓨터에서 실행

이제 프로그램의 일반 실행 모델이 명확 하 게 Q# 됩니다.

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

먼저 실행할 수 있는 특정 호출에는 동일한 네임 스페이스에 정의 된 다른 callables 및 형식에 대 한 액세스 권한이 있습니다.
또한 [ Q# 라이브러리](xref:microsoft.quantum.libraries)에서 액세스 하는 것은 물론, 전체 이름을 통하거나 위에 설명 된 문을 사용 하 여 참조 해야 합니다 `open` .

그런 다음 호출 가능 자체는 *[대상 컴퓨터](xref:microsoft.quantum.machines)* 에서 실행 됩니다.
이러한 대상 컴퓨터는 실제 퀀텀 하드웨어 이거나 QDK의 일부로 사용할 수 있는 여러 시뮬레이터 수 있습니다.
여기에서 가장 유용 하 게 사용할 수 있는 대상 컴퓨터는 [전체 상태 시뮬레이터](xref:microsoft.quantum.machines.full-state-simulator)의 인스턴스이고,이는 `QuantumSimulator` 프로그램의 동작을 의미 없는 퀀텀 컴퓨터에서 실행 되는 것 처럼 계산 합니다.

지금까지 특정 Q# 호출 가능이 실행 될 때 발생 하는 상황을 설명 했습니다.
Q#는 독립 실행형 응용 프로그램에서 사용 되는지에 관계 없이 호스트 프로그램에서 사용 되는지에 관계 없이이 일반적인 프로세스는---하 여 QDK 유연성을 사용 합니다.
따라서 퀀텀 개발 키트를 호출 하는 다양 한 방법 간의 차이점으로 인해 해당 호출 *how* 을 Q# 실행 하기 위해 호출 하는 방법 및 결과가 반환 되는 방식에도 표시 됩니다.
좀 더 구체적으로 말해서 차이를 중심으로 설명 합니다. 
1. Q#실행할 호출 가능 여부를 나타내는
2. 잠재적 호출 가능 인수가 제공 되는 방법
3. 실행 대상 컴퓨터를 지정 합니다.
4. 결과가 반환 되는 방법입니다.

먼저 명령 프롬프트에서 독립 실행형 응용 프로그램을 사용 하 여이 작업을 수행한 Q# 다음 Python 및 c # 호스트 프로그램을 사용 하 여이 작업을 진행 하는 방법을 설명 합니다.
Q#처음 세 가지가 아닌 주 기능이 로컬 파일을 중심으로 하지 않기 때문에 처음에는 jupyter 노트북의 독립 실행형 응용 프로그램을 예약 합니다 Q# .

> [!NOTE]
> 이러한 예에서 설명 하지는 않지만, 실행 메서드 간의 공통점은 프로그램 내부에서 인쇄 되는 모든 메시지 Q# ( [`Message`](xref:microsoft.quantum.intrinsic.message) [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) 예: 또는)가 일반적으로 해당 콘솔에 항상 인쇄 된다는 것입니다.

## <a name="no-locq-from-the-command-prompt"></a>Q# 명령 프롬프트에서
프로그램 작성을 시작 하는 가장 쉬운 방법 중 하나는 Q# 별도의 파일과 두 번째 언어를 함께 사용 하는 것을 걱정 하지 않는 것입니다.
QDK 확장과 함께 Visual Studio Code 또는 Visual Studio를 사용 하면 Q# 단일 파일 에서만 callables을 실행 하는 원활한 워크플로를 사용할 수 있습니다 Q# .

이렇게 하려면 다음을 입력 하 여 프로그램 실행을 궁극적으로 호출 합니다.
```dotnetcli
dotnet run
```
명령 프롬프트에서
가장 간단한 워크플로는 터미널의 디렉터리 위치가 파일과 동일 하 여 Q# Q# VS Code에서 통합 터미널을 사용 하 여 파일 편집과 함께 쉽게 처리할 수 있는 경우입니다.
그러나이 [ `dotnet run` 명령은](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) 다양 한 옵션을 허용 하며, `--project <PATH>` 파일의 위치를 단순히 제공 하 여 다른 위치에서 프로그램을 실행할 수도 있습니다 Q# .


### <a name="add-entry-point-to-no-locq-file"></a>파일에 진입점 추가 Q#

대부분의 Q# 파일에는 두 개 이상의 호출 가능이 포함 되어 있으므로 기본적으로 컴파일러에서 *which* 명령을 제공할 때 실행할 호출 가능 항목을 알 수 있도록 해야 합니다 `dotnet run` .
이렇게 하려면 파일 자체에 대 한 간단한 변경 작업을 수행 합니다 Q# . 
    - 호출 가능 바로 앞에를 사용 하 여 줄을 추가 `@EntryPoint()` 합니다.

따라서 위의 파일이 다음과 같은 상태가 됩니다.
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

이제 `dotnet run` 명령 프롬프트에서를 호출 하면 `MeasureSuperposition` 실행 되 고 반환 된 값이 터미널에 직접 인쇄 됩니다.
따라서 또는이 인쇄 된 것을 볼 수 있습니다 `One` `Zero` . 

아래에 더 많은 callables을 정의 하는 경우에는 문제가 되지 않습니다 `MeasureSuperposition` .
또한 선언 전에 호출 가능한 [문서 주석을](xref:microsoft.quantum.guide.filestructure#documentation-comments) 포함 하는 경우에는이 `@EntryPoint()` 특성을 위에 배치 하면 됩니다.

### <a name="callable-arguments"></a>호출 가능 인수

지금까지 입력을 받지 않는 작업만 고려 했습니다.
비슷한 작업을 수행 하려고 하지만 여러 가지 작업에서 인수로 제공 되는 수를---한다고 가정 합니다.
이러한 작업은 다음으로 작성 될 수 있습니다.
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
여기서 반환 된 값은 측정 결과의 배열입니다.
및는 [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) [`ForEach`](xref:microsoft.quantum.arrays.foreach) [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) 및 네임 스페이스에 있으므로 [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) `open` 각에 대 한 추가 문이 필요 합니다.

`@EntryPoint()`이 새 작업 앞에 특성을 이동 하는 경우 (참고: 파일에는 해당 줄이 하나만 있을 수 있음),이 작업을 실행 하려고 하면 `dotnet run` 추가 명령줄 옵션이 필요한 것을 나타내는 오류 메시지와이를 표현 하는 방법이 표시 됩니다.

명령줄에 대 한 일반 형식은 실제로 이며 `dotnet run [options]` 호출 가능 인수가 여기에 제공 됩니다.
이 경우 인수가 `n` 누락 되 고 옵션을 제공 해야 함을 보여 줍니다 `-n <n>` . `MeasureSuperpositionArray`이제는를 사용 하 여를 실행 합니다. `n=4`

```dotnetcli
dotnet run -n 4
```

다음과 유사한 출력을 생성 합니다.

```output
[Zero,One,One,One]
```

이 과정에서 여러 인수를 확장 합니다.

> [!NOTE]
> 에 정의 된 인수 이름은 `camelCase` 컴파일러에 의해 입력으로 허용 되도록 약간 변경 됩니다 Q# . 예를 들어, 대신 `n` 위의 이름을 사용한 경우 `numQubits` 이 입력은 대신를 통해 명령줄에서 제공 됩니다 `--num-qubits 4` `-n 4` .

또한이 오류 메시지는 대상 컴퓨터를 변경 하는 방법을 포함 하 여 사용할 수 있는 다른 옵션을 제공 합니다.

### <a name="different-target-machines"></a>다른 대상 컴퓨터

지금까지 작업의 출력은 실제 환경에서 작업의 예상 결과를 가지 며, 명령줄의 기본 대상 컴퓨터가 전체 상태 퀀텀 시뮬레이터 인 것을 알 수 `QuantumSimulator` 있습니다.
그러나 옵션 `--simulator` (또는 약식)을 사용 하 여 특정 대상 컴퓨터에서 실행 되도록 callables에 지시할 수 있습니다 `-s` .

예를 들어, 다음에서 실행할 수 있습니다 [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) .

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

인쇄 된 출력은

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

이러한 메트릭에 표시 되는 내용에 대 한 자세한 내용은 [Resource 평가기: 보고 된 메트릭](xref:microsoft.quantum.machines.resources-estimator#metrics-reported)을 참조 하세요.

### <a name="command-line-execution-summary"></a>명령줄 실행 요약
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a>옵션이 아닌 Q# `dotnet run`

위에서 언급 한 옵션을 사용 하 여 위에서 언급 한 것 처럼 `--project` 이 [ `dotnet run` 명령은](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) 호출 가능 인수와 관련이 없는 옵션도 허용 Q# 합니다.
두 종류의 옵션을 모두 제공 하는 경우 `dotnet` 관련 옵션을 먼저 제공 하 고 그 다음에 구분 기호가를 입력 한 다음 관련 옵션을 제공 해야 합니다 `--` Q# .
예를 들어 위의 작업에 대 한 숫자 값과 함께 경로를 지정 하 여를 통해 실행 `dotnet run --project <PATH> -- -n <n>` 합니다.

## <a name="no-locq-with-host-programs"></a>Q# 호스트 프로그램 사용

직접 파일을 사용 하는 경우 Q# 명령 프롬프트에서 직접 작업 또는 함수를 호출 하는 대신 다른 기존 언어로 *호스트 프로그램* 을 사용할 수 있습니다. 특히 c # 또는 F # 등의 .NET 언어를 사용 하 여이 작업을 수행할 수 있습니다 .이를 위해 c # 또는 F #과 같은 .NET 언어를 사용 하 여이 작업을 수행할 수 있습니다.
상호 운용성을 사용 하려면 약간의 설정이 필요 하지만 이러한 세부 정보는 [설치 가이드](xref:microsoft.quantum.install)에서 찾을 수 있습니다.

간단히 말해서, 이러한 상황에는 `*.py` `*.cs` 파일과 동일한 위치에 호스트 프로그램 파일 (예: 또는)이 포함 되어 있습니다 Q# .
이제 실행 되는 *호스트* 프로그램이 실행 되는 과정에서 파일의 특정 Q# 작업 및 함수를 호출할 수 있습니다 Q# .
상호 운용성의 핵심은 Q# Q# 호출 될 수 있도록 호스트 프로그램에서 파일의 콘텐츠를 액세스할 수 있도록 하는 컴파일러를 기반으로 합니다.

호스트 프로그램을 사용할 때의 주요 이점 중 하나는 프로그램에서 반환 된 기존 데이터가 Q# 호스트 언어로 추가로 처리 될 수 있다는 것입니다.
이는 일부 고급 데이터 처리 (예:에서 내부적으로 수행 될 수 없는 항목)로 구성 될 수 Q# 있으며, Q# 그 결과에 따라 추가 작업을 호출 하거나 결과를 그리는 것 처럼 간단 하 게 처리할 수 있습니다. Q#

일반적인 체계는 다음과 같습니다. 여기에서는 Python 및 c #에 대 한 특정 구현을 설명 합니다. F # 호스트 프로그램을 사용 하는 샘플은 [.net 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet)에서 찾을 수 있습니다.

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> `@EntryPoint()`응용 프로그램에 사용 되는 특성은 Q# 호스트 프로그램과 함께 사용할 수 없습니다.
> 호스트에서 호출 하는 파일에 있는 경우 오류가 발생 합니다 Q# . 

다른 호스트 프로그램을 사용 하려면 파일에 필요한 변경 내용이 없습니다 `*.qs` Q# .
다음 호스트 프로그램 구현은 모두 동일한 파일을 사용 하 여 작업 합니다 Q# .

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

원하는 호스트 언어에 해당 하는 탭을 선택 합니다.

### <a name="python"></a>[Python](#tab/tabid-python)
Python 호스트 프로그램은 다음과 같이 구성 됩니다.
1. 모듈 `qsharp` 을 가져옵니다 .이 모듈은 상호 운용성을 위해 모듈 로더를 등록 합니다 Q# . 
    이렇게 하면 Q# 네임 스페이스를 Python 모듈로 표시 하 여 "가져오기" 호출을 수행할 수 있습니다 Q# .
    기술적으로는 가져올 수 있는 것이 아니라이를 Q# 호출할 수 있는 Python 스텁을 사용 합니다.
    그런 다음 메서드를 사용 하 여 실행을 위해 작업을 보낼 대상 컴퓨터를 지정 하는 Python 클래스의 개체로 동작 합니다.

2. Q#이 경우---를 직접 호출 하는 callables을 가져옵니다 `MeasureSuperposition` `MeasureSuperpositionArray` .
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    모듈을 가져온 후에는 `qsharp` 라이브러리 네임 스페이스에서 직접 callables을 가져올 수도 있습니다 Q# .

3. 다른 Python 코드 중에서 이제 특정 대상 컴퓨터에서이 호출을 호출 하 고, 나중에 사용할 수 있도록 해당 반환을 변수에 할당 (값을 반환 하는 경우) 할 수 있습니다.

#### <a name="specifying-target-machines"></a>대상 컴퓨터 지정
특정 대상 컴퓨터에서 실행 되도록 작업을 호출 하는 것은 가져온 개체에 대 한 다른 Python 메서드를 통해 수행 됩니다.
예를 들어,는를 사용 하 여 작업을 실행 하는 반면,는를 사용 하 여 `.simulate(<args>)` 작업을 실행 합니다 `QuantumSimulator` `.estimate_resources(<args>)` `ResourcesEstimator` .

#### <a name="passing-inputs-to-q"></a>Q에 입력 전달\#
호출 가능의 인수는 Q# 키워드 인수 형식으로 제공 해야 합니다. 여기서 키워드는 호출 가능 정의의 인수 이름입니다 Q# .
즉,는 `MeasureSuperpositionArray.simulate(n=4)` 유효 하지만는 `MeasureSuperpositionArray.simulate(4)` 오류를 throw 합니다.

따라서 Python 호스트 프로그램 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

결과는 다음과 유사 하 게 출력 됩니다.

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a>Q#다른 프로젝트 또는 패키지의 코드 사용

기본적으로이 `import qsharp` 명령은 현재 폴더의 모든 파일을 로드 `.qs` 하 고 Q# Python 스크립트 내에서 해당 작업 및 기능을 사용할 수 있도록 합니다.

Q#다른 폴더에서 코드를 로드 하기 위해 [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) 를 사용 하 여 `.csproj` 프로젝트에 대 한 파일 Q# (즉,를 참조 하는 프로젝트)에 대 한 참조를 추가할 수 있습니다 `Microsoft.Quantum.Sdk` .
이 명령은 `.qs` 및 하위 폴더가 들어 있는 폴더의 모든 파일을 컴파일합니다 `.csproj` . 또한를 통해 참조 되 `PackageReference` Q# 는 패키지나 해당 파일의를 통해 참조 되는 프로젝트를 재귀적으로 로드 `ProjectReference` `.csproj` 합니다.

예를 들어, 다음 Python 코드는 현재 폴더에 상대적인 경로를 참조 하 고 해당 작업 중 하나를 호출 하는 외부 프로젝트를 가져옵니다 Q# .

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

그러면 다음과 같이 출력 됩니다.

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

코드를 포함 하는 외부 패키지를 로드 하려면 Q# [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages)를 사용 합니다.

Q#현재 폴더의 코드가 외부 프로젝트 또는 패키지에 종속 `import qsharp` 된 경우 종속성이 아직 로드 되지 않았기 때문에 실행 시 오류가 표시 될 수 있습니다.
명령 중에 필요한 외부 패키지 또는 프로젝트를 로드 하려면 Python 스크립트를 포함 하는 Q# `import qsharp` 폴더에를 참조 하는 파일이 포함 되어 있는지 확인 `.csproj` `Microsoft.Quantum.Sdk` 합니다. 그런 다음 `.csproj` 속성을에 추가 `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` 합니다. 그러면 Q# `ProjectReference` `PackageReference` 명령 중에 찾은 항목이 나 항목을 재귀적으로 로드 `.csproj` `import qsharp` 합니다.

예를 들어 다음은 패키지를 `.csproj` Q# 자동으로 로드 하는 간단한 파일입니다 `Microsoft.Quantum.Chemistry` .

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> 현재이 사용자 지정 `<IQSharpLoadAutomatically>` 속성은 python 호스트에 필요 하지만 나중에 `.csproj` python 스크립트와 동일한 폴더에 있는 파일에 대 한 기본 동작이 될 수 있습니다.

> [!NOTE]
> 현재의 `<QsharpCompile>` 설정은 `.csproj` Python 호스트에서 무시 되 고 하위 폴더를 `.qs` 포함 하 여의 폴더에 있는 모든 파일이 `.csproj` 로드 되 고 컴파일됩니다. 나중에 설정에 대 한 지원이 `.csproj` 향상 됩니다 (자세한 내용은 [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) 참조).


### <a name="c"></a>[C#](#tab/tabid-csharp)

C # 호스트 프로그램에는 여러 구성 요소가 있으며, c #을 기반으로 하는 시뮬레이터와 같이 QDK 일부 구성 요소와 매우 긴밀 하 게 작동 합니다.

Q#컴파일러는 Q# 파일의 네임 스페이스에서 동등 하 게 명명 된 c # 네임 스페이스를 생성 하 여 여기에서 작업 합니다 Q# .
여기에 정의 된 각 callables 또는 형식에 대해 동등 하 게 명명 된 c # 클래스를 생성 Q# 합니다.

먼저 `using` 파일의 문과 거의 analagous 하는 문을 사용 하 여 호스트 프로그램에서 사용 되는 모든 클래스를 사용 하도록 설정 합니다 `open` Q# .

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

다음으로 c # 네임 스페이스, 몇 가지 다른 비트 및 부분 (아래의 전체 코드 블록 참조)을 선언 하 고 원하는 모든 기존 프로그래밍을 선언 합니다 (예: callables의 인수 계산 Q# ).
후자의 경우에는 후자를 사용할 필요가 없지만 이러한 사용의 예는  [.net 상호 운용성 샘플](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet)에서 찾을 수 있습니다.

#### <a name="target-machines"></a>대상 머신

로 돌아가서 Q# , 작업을 실행 하는 대상 컴퓨터의 인스턴스를 만들어야 합니다.

```csharp
            using var sim = new QuantumSimulator();
```

다른 대상 컴퓨터를 사용 하는 것은 다른 대상 컴퓨터를 인스턴스화하는 것 만큼 간단 합니다. 즉,이를 수행 하 고 반환을 처리 하는 방법은 약간 다를 수 있습니다.
간단 하 게 하기 위해 이제에는 [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [다음](#including-the-resources-estimator)이 포함 됩니다.

작업에서 생성 된 각 c # 클래스에는 Q# `Run` 메서드가 있습니다. 첫 번째 인수는 대상 컴퓨터 인스턴스여야 합니다.
따라서에서을 실행 하려면 `MeasureSuperposition` `QuantumSimulator` 를 사용 `MeasureSuperposition.Run(sim)` 합니다.
그러면 c #에서 반환 된 결과를 변수에 할당할 수 있습니다.

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> `Run`메서드는 실제 퀀텀 하드웨어의 경우에는 비동기적으로 실행 되므로 `await` 작업이 완료 될 때까지 키워드는 추가 실행을 차단 합니다.

호출에 Q# 반환 형식이 있는 반환 형식이 없는 경우에 `Unit` 도 실행은 변수에 할당 하지 않고 동일한 방식으로 수행할 수 있습니다.
이 경우 전체 줄은 다음과 같이 구성 됩니다. 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a>인수

호출 가능한에 대 한 모든 인수 Q# 는 대상 컴퓨터에 대 한 추가 인수로 전달 됩니다.
따라서에 대 한 결과는 다음을 `MeasureSuperpositionArray` `n=4` 통해 인출 됩니다. 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

따라서 전체 c # 호스트 프로그램은 다음과 같습니다.

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

C # 파일의 위치에서 다음을 입력 하 여 명령 프롬프트에서 호스트 프로그램을 실행할 수 있습니다.
```dotnetcli
dotnet run
```
이 경우 콘솔에 기록 된 출력이 다음과 유사 하 게 표시 됩니다. 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> 컴파일러는 네임 스페이스와의 상호 운용성 때문에 Q# 문 없이 callables을 사용할 수 있도록 설정 하 `using NamespaceName;` 고 c # 네임 스페이스 제목만 일치 시킬 수도 있습니다.
> 즉,를로 바꿉니다 `namespace host` `namespace NamespaceName` .

#### <a name="including-the-resources-estimator"></a>평가기 리소스 포함

에서 [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) 출력을 검색 하려면 약간 다른 구현이 필요 합니다.

첫째, 문을 사용 하 여 변수로 인스턴스화하는 대신 `using` (에서와 같이 `QuantumSimulator` ) 클래스의 개체를 직접 인스턴스화 합니다.

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

여러 작업에서 단일 대상 시뮬레이터를 사용 하는 대신 Q# 각각에 대해 하나씩 인스턴스화합니다. 이는 대상 컴퓨터로 사용 되는 경우 개체 자체가 수정 되 고 그 결과를 나중에 클래스 메서드를 사용 하 여 검색할 수 있기 때문입니다 `.ToTSV()` .

리소스 추정에 대 한 작업을 실행 하려면 다음을 사용 합니다.

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
그런 다음 및를 사용 하 여 TSV (탭으로 구분 된 값)로 결과를 인출 합니다 `estimatorSingleQ.ToTSV()` `estimatorMultiQ.ToTSV()` .

따라서 및를 모두 사용 하는 전체 c # 호스트 프로그램 `QuantumSimulator` 은 `ResourcesEstimator` 다음 형식을 사용할 수 있습니다.

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


그러면 다음과 유사한 출력이 생성 됩니다.

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a>Q# Jupyter 노트북
Q# Jupyter 노트북은 Q# Q# 모든 지침, 메모 및 기타 콘텐츠와 함께---단일 노트북에서 callables을 정의, 컴파일 및 실행할 수 있는 I 커널을 사용 합니다.
즉, 파일의 내용을 가져오고 사용할 수는 있지만 `*.qs` Q# 실행 모델에는 필요 하지 않습니다.

여기서는 위에 정의 된 작업을 실행 하는 방법에 대해 자세히 설명 Q# 하지만, jupyter 노트북을 사용 하는 방법에 대 한 더 광범위 한 소개는 Q# [ Q# 및 jupyter 노트북](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)에서 제공 됩니다.

### <a name="defining-operations"></a>작업 정의

Jupyter Notebook에서 Q# Q# 파일의 네임 스페이스 내에서와 같은 방식으로 코드를 입력 Q# 합니다.

따라서 해당 네임 스페이스에 대 한 문을 사용 하 여 [ Q# 표준 라이브러리](xref:microsoft.quantum.qsharplibintro) 에서 callables에 액세스 하도록 설정할 수 있습니다 `open` .
이러한 문을 사용 하 여 셀을 실행할 때 해당 네임 스페이스의 정의는 작업 영역 전체에서 사용할 수 있습니다.

> [!NOTE]
> [Microsoft](xref:microsoft.quantum.intrinsic) 에서 사용 하는 callables [(예](xref:microsoft.quantum.canon) : [`H`](xref:microsoft.quantum.intrinsic.h) 및 [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) )은 jupyter 노트북의 셀 내에 정의 된 작업에서 자동으로 사용할 수 있습니다. Q#
> 그러나 외부 소스 파일에서 가져온 코드 Q# ( [ Q# 및 Jupyter 노트북](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)에 표시 되는 프로세스)에는 적용 되지 않습니다. 
> 

마찬가지로 작업을 정의 하려면 코드를 작성 Q# 하 고 셀을 실행 하기만 하면 됩니다.

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="773">

그런 다음 출력에는 이후 셀에서 호출할 수 있는 해당 작업이 나열 됩니다.

### <a name="target-machines"></a>대상 머신

특정 대상 컴퓨터에서 작업을 실행 하는 기능은 [ Q# 매직 명령을](xref:microsoft.quantum.guide.quickref.iqsharp)통해 제공 됩니다.
예를 들어,를 `%simulate` 사용 하 `QuantumSimulator` 고는를 사용 `%estimate` 합니다 `ResourcesEstimator` .

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a Q# operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a>함수 및 작업에 입력 전달

작업에 입력을 전달 하기 위해 Q# 인수는 `key=value` 실행 매직 명령에 쌍으로 전달 될 수 있습니다.
따라서 `MeasureSuperpositionArray` 4 개의 비트를 사용 하 여를 실행 하려면 다음을 실행할 수 있습니다 `%simulate MeasureSuperpositionArray n=4` .

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a Q# operation with arguments" width="773">

이 패턴은 `%estimate` 및 기타 실행 명령과 유사 하 게 사용할 수 있습니다.

### <a name="using-no-locq-code-from-other-projects-or-packages"></a>Q#다른 프로젝트 또는 패키지의 코드 사용

기본적으로 Jupyter Notebook는 Q# `.qs` 현재 폴더에 있는 모든 파일을 로드 하 고 해당 Q# 작업 및 기능을 노트북 내부에서 사용할 수 있도록 합니다. [ `%who` 매직 명령은](xref:microsoft.quantum.iqsharp.magic-ref.who) 현재 사용할 수 있는 모든 Q# 작업 및 함수를 나열 합니다.

Q#다른 폴더에서 코드를 로드 하기 위해 [ `%project` 매직 명령은](xref:microsoft.quantum.iqsharp.magic-ref.project) `.csproj` 프로젝트에 대 한 파일 Q# (즉,를 참조 하는 프로젝트)에 대 한 참조를 추가 하는 데 사용할 수 있습니다 `Microsoft.Quantum.Sdk` . 이 명령은 `.qs` 및 하위 폴더를 포함 하는 폴더의 모든 파일을 컴파일합니다 `.csproj` . 또한를 통해 참조 되 `PackageReference` Q# 는 패키지나 해당 파일의를 통해 참조 되는 프로젝트를 재귀적으로 로드 `ProjectReference` `.csproj` 합니다. 

예를 들어 다음 셀은 Q# 외부 프로젝트에서 작업을 시뮬레이션 합니다. 여기서 프로젝트 경로는 현재 폴더를 기준으로 참조 됩니다.

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a Q# operation from an external project" width="773">

코드를 포함 하는 외부 패키지를 로드 하려면 Q# [ `%package` 매직 명령을](xref:microsoft.quantum.iqsharp.magic-ref.package)사용 합니다.
패키지를 로드 하면 사용자 지정 매직 명령이 나 패키지의 일부인 모든 어셈블리에 포함 된 인코더 표시도 가능 합니다.

노트북 초기화 시간에 외부 패키지 또는 프로젝트를 로드 하려면 노트북 폴더에를 참조 하는 Q# 파일이 포함 되어 있는지 확인 `.csproj` `Microsoft.Quantum.Sdk` 합니다. 그런 다음 `.csproj` 속성을에 추가 `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` 합니다. 이렇게 하면 Q# `ProjectReference` `PackageReference` 노트북 로드 시에 발견 된 항목 또는 항목을 재귀적으로 로드 하는 것을 알려 `.csproj` 줍니다.

예를 들어 다음은 패키지를 `.csproj` Q# 자동으로 로드 하는 간단한 파일입니다 `Microsoft.Quantum.Chemistry` .

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> 현재이 사용자 지정 `<IQSharpLoadAutomatically>` 속성은 Q# Jupyter Notebook 호스트에 필요 하지만 나중에 `.csproj` 전자 필기장 파일과 동일한 폴더에 있는 파일에 대 한 기본 동작이 될 수 있습니다.

> [!NOTE]
> 현재의 `<QsharpCompile>` 설정은 `.csproj` Jupyter Notebook 호스트에서 무시 되 Q# 고 하위 폴더를 `.qs` 포함 하 여의 폴더에 있는 모든 파일이 `.csproj` 로드 되 고 컴파일됩니다. 나중에 설정에 대 한 지원이 `.csproj` 향상 됩니다 (자세한 내용은 [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) 참조).
