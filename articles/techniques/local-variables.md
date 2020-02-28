---
title: '지역 변수-Q # 기술'
description: 'Q #에서 지역 변수를 정의 하 고 사용 하는 방법에 대해 알아봅니다.'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.local-variables
ms.openlocfilehash: cb6c662137c31a13c3dd6e9ca3f67879c469f788
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906868"
---
# <a name="local-variables"></a><span data-ttu-id="637af-103">지역 변수</span><span class="sxs-lookup"><span data-stu-id="637af-103">Local Variables</span></span> #

<span data-ttu-id="637af-104">`let` 키워드를 사용 하 여 작업 또는 함수 내에서 다시 사용 하기 위해 Q #의 모든 형식 값을 변수에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-104">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>
<span data-ttu-id="637af-105">예:</span><span class="sxs-lookup"><span data-stu-id="637af-105">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="637af-106">이렇게 하면 `measurementOperator`라는 변수에 Pauli 연산자의 특정 배열이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="637af-106">This assigns a particular array of Pauli operators to a variable called `measurementOperator`.</span></span>

> [!TIP]
> <span data-ttu-id="637af-107">`let` 문의 오른쪽에 있는 식이 명확 하 고 형식이 컴파일러에 의해 유추 되기 때문에 새 변수의 형식을 명시적으로 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-107">Note that we did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="637af-108">Q #의 변수는 *변경할*수 없습니다. 즉, 변수를 이러한 방식으로 정의한 후에는 어떤 방식으로든 더 이상 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-108">Variables in Q# are *immutable*, meaning that once a variable has been defined in this way, it can no longer be changed in any way.</span></span>
<span data-ttu-id="637af-109">이렇게 하면 작업의 `Adjoint` 변형을 적용 하기 위해 다시 정렬할 변수에 적용 되는 기존 논리의 최적화를 비롯 하 여 여러 가지 유용한 최적화를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-109">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

<span data-ttu-id="637af-110">위와 같이 `let` 바인딩을 사용 하 여 정의 된 변수는 작업의 본문이 나 `for` 루프의 내용과 같은 특정 범위에 대해 로컬입니다.</span><span class="sxs-lookup"><span data-stu-id="637af-110">Variables defined using the `let` binding as above are local to a particular scope, such as the body of an operation or the contents of a `for` loop.</span></span>


## <a name="mutability"></a><span data-ttu-id="637af-111">가변성</span><span class="sxs-lookup"><span data-stu-id="637af-111">Mutability</span></span> ##

<span data-ttu-id="637af-112">`let`를 사용 하 여 변수를 만드는 대신 `mutable` 키워드는 `set` 키워드를 사용 하 여 처음 생성 된 후에 다시 바인딩할 수 있는 특수 한 변경 가능한 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="637af-112">As an alternative to creating a variable with `let`, the `mutable` keyword will create a special mutable variable that can be re-bound after it is initially created by using the `set` keyword.</span></span>

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

<span data-ttu-id="637af-113">Q #에서 배열을 비롯 한 모든 형식은 값 의미 체계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="637af-113">All types in Q#, including arrays, follow value semantics.</span></span> <span data-ttu-id="637af-114">특히 배열 항목을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-114">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="637af-115">기존 배열을 수정 하려면의 F#레코드에 대 한 것과 매우 유사한 복사 및 업데이트 메커니즘을 활용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="637af-115">To modify an existing array requires leveraging a copy-and-update mechanism much like the one for records in F#.</span></span> <span data-ttu-id="637af-116">[`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays)에서 제공 하는 배열에 대해 라이브러리 도구를 사용 하 여, 예를 들어, paulis의 배열을 반환 하는 함수를 쉽게 정의할 수 있습니다. 여기서는 인덱스 `i`의 Paulis가 지정 된 값을 사용 하 고 다른 모든 항목은 id입니다.</span><span class="sxs-lookup"><span data-stu-id="637af-116">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can e.g. easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity:</span></span> 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

<span data-ttu-id="637af-117">Q # 문과 식을 설명할 때 배열을 사용 하는 방법에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="637af-117">We will elaborate more on how to work with arrays when discussing Q# statements and expressions.</span></span> 

<span data-ttu-id="637af-118">Q # 내의 가변성는 형식 또는 값이 아닌 *기호* 에 적용 되는 개념입니다.</span><span class="sxs-lookup"><span data-stu-id="637af-118">Mutability within Q# is a concept that applies to a *symbol* rather than a type or value.</span></span> <span data-ttu-id="637af-119">구체적으로는 형식 시스템에 암시적 또는 명시적으로 표시 되지 않고 바인딩을 변경할 수 있는지 (`mutable` 키워드에 의해 표시 된 대로) 또는 변경 불가능 (`let`에 의해 표시 됨)에 대 한 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-119">Specifically, it does not have a representation in the type system, implicitly or explicitly, and whether or not a binding is mutable (as indicated by the `mutable` keyword) or immutable (as indicated by `let`) does not change the type of the bound variable(s).</span></span> <span data-ttu-id="637af-120">이는 특수화 된 함수 및 작업 내에서 가변성를 격리 하는 중요 한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="637af-120">This provides an important way to isolate mutability inside specialized functions and operations.</span></span>
<span data-ttu-id="637af-121">특히 변경 가능한 변수를 사용 하는 작업에 대 한 adjoint 특수화가 자동 생성 될 수 없는 경우에도 자동 생성은 가변성를 사용 하는 함수를 호출 하는 작업에 대해 제대로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="637af-121">In particular, even though an adjoint specialization for an operation which uses a mutable variable cannot be auto-generated, auto-generation works fine for an operation calling a function which uses mutability.</span></span>
<span data-ttu-id="637af-122">이러한 이유로 가변성를 사용 하는 함수 및 작업을 가능한 한 간단 하 고 간결한 방식으로 설정 하는 것이 좋습니다. 이렇게 하면 변경 불가능 한 일반 변수를 사용 하 여 나머지 퀀텀 프로그램을 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-122">For this reason, it is a good practice to make functions and operations which use mutability as short and compact as possible, so that the rest of the quantum program can be written using ordinary immutable variables.</span></span>


## <a name="deconstruction"></a><span data-ttu-id="637af-123">분해</span><span class="sxs-lookup"><span data-stu-id="637af-123">Deconstruction</span></span> ##

<span data-ttu-id="637af-124">단일 변수를 할당 하는 것 외에도 `let` 및 `mutable` 키워드를 사용 하거나, 다른 바인딩 구문을 사용 하 여 [튜플 형식의](xref:microsoft.quantum.language.type-model#tuple-types)콘텐츠를 압축 풀기도 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="637af-124">In addition to assigning a single variable, the `let` and `mutable` keywords - or in fact any other binding construct - also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.language.type-model#tuple-types).</span></span>
<span data-ttu-id="637af-125">이 폼의 할당은 해당 튜플의 요소를 *분해할* 하는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="637af-125">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>
<span data-ttu-id="637af-126">예를 들어 튜플에 의해 Hamiltonian에서 용어를 모델링 하는 경우 분해를 사용 하 여 해당 용어로 시뮬레이트하는 데 필요한 다양 한 데이터에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="637af-126">For instance, if we model a term in a Hamiltonian by a tuple, then we can use deconstruction to access the different data that we need to simulate under that term:</span></span>

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```


