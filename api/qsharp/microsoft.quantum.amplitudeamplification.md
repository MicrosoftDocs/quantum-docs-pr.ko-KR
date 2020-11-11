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
# <a name="microsoftquantumamplitudeamplification-namespace"></a><span data-ttu-id="60ea2-102">AmplitudeAmplification 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="60ea2-102">Microsoft.Quantum.AmplitudeAmplification namespace</span></span>

<span data-ttu-id="60ea2-103">이 네임 스페이스는 진폭 증폭을 수행 하기 위한 함수 및 작업을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-103">This namespace contains functions and operations for performing amplitude amplification.</span></span>



## <a name="description"></a><span data-ttu-id="60ea2-104">Description</span><span class="sxs-lookup"><span data-stu-id="60ea2-104">Description</span></span>

<span data-ttu-id="60ea2-105">부분 반사를 포함 하는 명확한 진폭 증폭은 여기에서 구현 되는 가장 일반적인 형식의 진폭 증폭입니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-105">Oblivious amplitude amplification with partial reflections is the most general form of amplitude amplification implemented here.</span></span>

<span data-ttu-id="60ea2-106">이는 AmpAmpObliviousByReflectionPhases 작업을 통해 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-106">This is called through the operation AmpAmpObliviousByReflectionPhases.</span></span>

<span data-ttu-id="60ea2-107">여기에는 및의 두 레지스터가 있습니다. `ancillaRegister` `systemRegister`</span><span class="sxs-lookup"><span data-stu-id="60ea2-107">This has two registers: `ancillaRegister` and `systemRegister`.</span></span>

<span data-ttu-id="60ea2-108">이는 `ReflectionOracle` 레지스터에만 작동 하는 형식의 이러한 리플렉션에 대해 두 개의 oracles를 허용 합니다 `ancillaRegister` .</span><span class="sxs-lookup"><span data-stu-id="60ea2-108">This accepts two oracles for these reflections of type `ReflectionOracle` which act only on the `ancillaRegister` register.</span></span>

<span data-ttu-id="60ea2-109">이를 통해 `ObliviousOracle` 두 레지스터 모두에 대해 공동으로 작동 하는 형식의 명확한 진폭 증폭을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-109">This accepts an oracle special to oblivious amplitude amplification of type `ObliviousOracle` which acts jointly on both register.</span></span>

<span data-ttu-id="60ea2-110">에 대 한 입력 상태는 `ancillaRegister` 첫 번째 리플렉션 연산자 $I-2 \ k {s} \ bra {s} $의 고유한 $-$1 eigenstate로 가정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-110">The input state to `ancillaRegister` is assumed to be the unique $-1$ eigenstate of the first reflection operator $I - 2\ket{s}\bra{s}$.</span></span>

<span data-ttu-id="60ea2-111">대상 퀀텀 상태에 대 한 반사는 계산 기준 $ \ket{0\cdots 0} $에서 해당 상태를 준비 하는 oracle에 대 한 액세스를 가정 하 여 구현 되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-111">Reflections about a target quantum state are often implemented by assuming access to an oracle that prepare that state from the computational basis $\ket{0\cdots 0}$.</span></span>

<span data-ttu-id="60ea2-112">이러한 oracles에 대 한 규칙에는 단일 요구 비트 레지스터의 두 레지스터 `flagQubit` 와 다른 모든 항목에 대 한 레지스터가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-112">Our convention for these oracles requires two registers: a single-qubit `flagQubit` register, and a register for everything else on the ancillaRegister register.</span></span>

<span data-ttu-id="60ea2-113">형식의 oracle은 `StateOracle` 두 레지스터를 공동으로 사용 하 여 {1} `flagQubit` 일부 실제 진폭 등록에서 $ \ket $로 플래그가 지정 된 대상 상태를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-113">The oracle of type `StateOracle` acts jointly on both registers to create the target state flagged by $\ket{1}$ in the `flagQubit` register with some real amplitude.</span></span>

<span data-ttu-id="60ea2-114">`ReflectionOracle`이 플래그 상태에 대 한 리플렉션은 작업에서 생성 됩니다 `TargetStateReflectionOracle` .</span><span class="sxs-lookup"><span data-stu-id="60ea2-114">The reflection `ReflectionOracle` about the this flag state is generated by the operation `TargetStateReflectionOracle`.</span></span>

<span data-ttu-id="60ea2-115">`ReflectionOracle`에 대 한 입력 상태에 대 한 리플렉션은 상태를 `ancillaRegister` 반전 시킨 다음 ReflectionStart ()와 함께 $ \ket{0\cdots 0} $를 반영 하 여 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-115">The reflection `ReflectionOracle` about the input state to `ancillaRegister` is generated by the inverting StateOracle and then reflecting about $\ket{0\cdots 0}$ with ReflectionStart().</span></span>

<span data-ttu-id="60ea2-116">형식의 oracle은 `DeterministicStateOracle` 레지스터에 대해 작동 `qubitState` 하 여 플래그가 없는 상태에서 정확히 대상 상태를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-116">The oracle of type `DeterministicStateOracle` acts on the `qubitState` registers to create the target state exactly with no flag.</span></span>

<span data-ttu-id="60ea2-117">`AmpAmpObliviousByOraclePhases` 는 반사 대신 oracles 및를 허용 하는 명확한 진폭 증폭의 버전입니다 `StateOracle` `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="60ea2-117">`AmpAmpObliviousByOraclePhases` is a version of oblivious amplitude amplification that accepts oracles `StateOracle` and `ObliviousOracle` instead of reflections.</span></span>

<span data-ttu-id="60ea2-118">진폭 증폭은 명확한 진폭 증폭의 특별 한 사례입니다. 여기서 `ObliviousOracle` 는 identity 연산자이 고 시스템의 경우는 비어 있습니다. `systemRegister`</span><span class="sxs-lookup"><span data-stu-id="60ea2-118">Note that amplitude amplification is a special case of oblivious amplitude amplification where `ObliviousOracle` is the identity operator, and there are no system qubits i.e. `systemRegister` is empty.</span></span>

<span data-ttu-id="60ea2-119">이 작업은 및 작업을 통해 호출 됩니다 `AmpAmByReflectionPhases` `AmpAmpByOraclePhases` .</span><span class="sxs-lookup"><span data-stu-id="60ea2-119">This is called through the operation `AmpAmByReflectionPhases` and `AmpAmpByOraclePhases`.</span></span>

<span data-ttu-id="60ea2-120">Grover 검색의 표준 사례에서 부분 반사를 위한 단계는 AmpAmpPhasesStandard 함수에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-120">The phases for partial reflections in the standard case of Grover search is provided by the function AmpAmpPhasesStandard.</span></span>

<span data-ttu-id="60ea2-121">예를 들어 AmpAmpByOracle-> AmpAmpByOraclePhases > > AmpAmpObliviousByReflectionPhases와 같은 종속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60ea2-121">For instance, we have the following dependencies: AmpAmpByOracle -> AmpAmpByOraclePhases -> AmpAmpObliviousByOraclePhases -> AmpAmpObliviousByReflectionPhases.</span></span>