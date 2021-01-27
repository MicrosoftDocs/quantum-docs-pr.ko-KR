---
uid: Microsoft.Quantum.Oracles.OracleToDiscrete
title: OracleToDiscrete 함수
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: OracleToDiscrete
qsharp.summary: Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.
ms.openlocfilehash: ab59cdf0ab05092a9d4e7856b7808b13df655571
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842531"
---
# <a name="oracletodiscrete-function"></a><span data-ttu-id="5e5e7-102">OracleToDiscrete 함수</span><span class="sxs-lookup"><span data-stu-id="5e5e7-102">OracleToDiscrete function</span></span>

<span data-ttu-id="5e5e7-103">네임 스페이스: [Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="5e5e7-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="5e5e7-104">패키지: [Microsoft 양자 표준](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5e5e7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5e5e7-105">"블랙 박스" oracle을 나타내는 작업을 수행 하는 경우 "블랙 박스" oracle을 여러 번 반복 하는 불연속 시간 oracle이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-105">Given an operation representing a "black-box" oracle, returns a discrete-time oracle which represents the "black-box" oracle repeated multiple times.</span></span>

```qsharp
function OracleToDiscrete (blackBoxOracle : (Qubit[] => Unit is Adj + Ctl)) : Microsoft.Quantum.Oracles.DiscreteOracle
```


## <a name="input"></a><span data-ttu-id="5e5e7-106">입력</span><span class="sxs-lookup"><span data-stu-id="5e5e7-106">Input</span></span>

### <a name="blackboxoracle--qubit--unit--is-adj--ctl"></a><span data-ttu-id="5e5e7-107">블랙 박스 [oracle: Adj](xref:microsoft.quantum.lang-ref.qubit)+ Ctl의> [Unit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5e5e7-107">blackBoxOracle : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5e5e7-108">지수화 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-108">The operation to be exponentiated.</span></span>



## <a name="output--discreteoracle"></a><span data-ttu-id="5e5e7-109">출력: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="5e5e7-109">Output : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="5e5e7-110">불연속 시간 oracle을 나타내는 "블랙 박스" oracle에 부분적으로 적용 된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5e7-110">An operation partially applied over the "black-box" oracle representing the discrete-time oracle</span></span>

## <a name="example"></a><span data-ttu-id="5e5e7-111">예</span><span class="sxs-lookup"><span data-stu-id="5e5e7-111">Example</span></span>

<span data-ttu-id="5e5e7-112">`OracleToDiscrete(U)(3, target)` 는 세 번 반복 되는 것과 같습니다 `U(target)` .</span><span class="sxs-lookup"><span data-stu-id="5e5e7-112">`OracleToDiscrete(U)(3, target)` is equivalent to `U(target)` repeated three times.</span></span>