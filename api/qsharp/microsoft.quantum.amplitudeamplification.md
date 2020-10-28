---
uid: Microsoft.Quantum.AmplitudeAmplification
title: AmplitudeAmplification 네임 스페이스
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: 09c29bd9d0648bb8652051ad97ceca6ef6557df3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721845"
---
# <a name="microsoftquantumamplitudeamplification-namespace"></a>AmplitudeAmplification 네임 스페이스

이 네임 스페이스는 진폭 증폭을 수행 하기 위한 함수 및 작업을 포함 합니다.



## <a name="description"></a>Description

부분 반사를 포함 하는 명확한 진폭 증폭은 여기에서 구현 되는 가장 일반적인 형식의 진폭 증폭입니다.

이는 AmpAmpObliviousByReflectionPhases 작업을 통해 호출 됩니다.

여기에는 및의 두 레지스터가 있습니다. `ancillaRegister` `systemRegister`

이는 `ReflectionOracle` 레지스터에만 작동 하는 형식의 이러한 리플렉션에 대해 두 개의 oracles를 허용 합니다 `ancillaRegister` .

이를 통해 `ObliviousOracle` 두 레지스터 모두에 대해 공동으로 작동 하는 형식의 명확한 진폭 증폭을 사용할 수 있습니다.

에 대 한 입력 상태는 `ancillaRegister` 첫 번째 리플렉션 연산자 $I-2 \ k {s} \ bra {s} $의 고유한 $-$1 eigenstate로 가정 됩니다.

대상 퀀텀 상태에 대 한 반사는 계산 기준 $ \ket{0\cdots 0} $에서 해당 상태를 준비 하는 oracle에 대 한 액세스를 가정 하 여 구현 되는 경우가 많습니다.

이러한 oracles에 대 한 규칙에는 단일 요구 비트 레지스터의 두 레지스터 `flagQubit` 와 다른 모든 항목에 대 한 레지스터가 필요 합니다.

형식의 oracle은 `StateOracle` 두 레지스터를 공동으로 사용 하 여 {1} `flagQubit` 일부 실제 진폭 등록에서 $ \ket $로 플래그가 지정 된 대상 상태를 만듭니다.

`ReflectionOracle`이 플래그 상태에 대 한 리플렉션은 작업에서 생성 됩니다 `TargetStateReflectionOracle` .

`ReflectionOracle`에 대 한 입력 상태에 대 한 리플렉션은 상태를 `ancillaRegister` 반전 시킨 다음 ReflectionStart ()와 함께 $ \ket{0\cdots 0} $를 반영 하 여 생성 됩니다.

형식의 oracle은 `DeterministicStateOracle` 레지스터에 대해 작동 `qubitState` 하 여 플래그가 없는 상태에서 정확히 대상 상태를 만듭니다.

`AmpAmpObliviousByOraclePhases` 는 반사 대신 oracles 및를 허용 하는 명확한 진폭 증폭의 버전입니다 `StateOracle` `ObliviousOracle` .

진폭 증폭은 명확한 진폭 증폭의 특별 한 사례입니다. 여기서 `ObliviousOracle` 는 identity 연산자이 고 시스템의 경우는 비어 있습니다. `systemRegister`

이 작업은 및 작업을 통해 호출 됩니다 `AmpAmByReflectionPhases` `AmpAmpByOraclePhases` .

Grover 검색의 표준 사례에서 부분 반사를 위한 단계는 AmpAmpPhasesStandard 함수에서 제공 됩니다.

예를 들어 AmpAmpByOracle-> AmpAmpByOraclePhases > > AmpAmpObliviousByReflectionPhases와 같은 종속성이 있습니다.