---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: OracleToDiscrete 함수
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: d26d57c587f24e7f74102c12753bcddb00fd8a9d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724246"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="40756-102">OracleToDiscrete 함수</span><span class="sxs-lookup"><span data-stu-id="40756-102">OracleToDiscrete function</span></span>

<span data-ttu-id="40756-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="40756-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="40756-104">패키지 [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40756-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40756-105">"블랙 박스" oracle을 나타내는 작업을 수행 하는 경우 "블랙 박스" oracle을 여러 번 반복 하는 불연속 시간 oracle이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40756-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="40756-106">입력</span><span class="sxs-lookup"><span data-stu-id="40756-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit-adj--ctl"></a><span data-ttu-id="40756-107">블랙 박스 [oracle: [](xref:microsoft.quantum.lang-ref.qubit)] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span><span class="sxs-lookup"><span data-stu-id="40756-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="40756-108">지수화 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="40756-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="40756-109">출력: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="40756-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="40756-110">불연속 시간 oracle을 나타내는 "블랙 박스" oracle에 부분적으로 적용 된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="40756-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>