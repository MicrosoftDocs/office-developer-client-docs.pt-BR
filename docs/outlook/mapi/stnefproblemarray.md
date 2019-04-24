---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336495"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="e03ed-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="e03ed-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="e03ed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e03ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e03ed-105">Contém uma matriz de estruturas **STnefProblem** que descreve um ou mais problemas de processamento que ocorreram durante a codificação ou a decodificação de um fluxo de formato de encapsulamento neutro de transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="e03ed-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e03ed-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e03ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="e03ed-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="e03ed-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="e03ed-108">Members</span><span class="sxs-lookup"><span data-stu-id="e03ed-108">Members</span></span>

 <span data-ttu-id="e03ed-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="e03ed-109">**cProblem**</span></span>
  
> <span data-ttu-id="e03ed-110">Contagem de elementos na matriz especificada no membro **aproblem** .</span><span class="sxs-lookup"><span data-stu-id="e03ed-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="e03ed-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="e03ed-111">**aProblem**</span></span>
  
> <span data-ttu-id="e03ed-112">Matriz de estruturas [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="e03ed-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="e03ed-113">Cada estrutura contém informações sobre um problema de processamento de propriedade ou de atributo.</span><span class="sxs-lookup"><span data-stu-id="e03ed-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e03ed-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e03ed-114">Remarks</span></span>

<span data-ttu-id="e03ed-115">Se ocorrer um problema durante o processamento de atributo ou propriedade, um parâmetro de saída no método [ITnef:: ExtractProps](itnef-extractprops.md) e no método [ITnef:: Finish](itnef-finish.md) cada receberá um ponteiro para uma estrutura **STnefProblemArray** e \*\*ExtractProps \*\*e **Finalize** cada retorno do valor MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="e03ed-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="e03ed-116">Esse valor de erro indica que um problema surgiu durante o processamento e uma estrutura **STnefProblemArray** foi gerada.</span><span class="sxs-lookup"><span data-stu-id="e03ed-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="e03ed-117">Se uma estrutura **STnefProblem** não for gerada durante o processamento de um atributo ou propriedade, o aplicativo cliente poderá continuar com a suposição de que o processamento desse atributo ou propriedade tenha sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e03ed-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="e03ed-118">A única exceção ocorre quando o problema surgiu durante a decodificação de um bloco de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="e03ed-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="e03ed-119">Se o erro ocorreu durante essa decodificação, MAPI_E_UNABLE_TO_COMPLETE pode ser retornado como o [SCODE](scode.md) na estrutura.</span><span class="sxs-lookup"><span data-stu-id="e03ed-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="e03ed-120">Nesse caso, a decodificação do componente correspondente ao bloco é interrompida e a decodificação continua em outro componente.</span><span class="sxs-lookup"><span data-stu-id="e03ed-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e03ed-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e03ed-121">See also</span></span>



[<span data-ttu-id="e03ed-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="e03ed-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="e03ed-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="e03ed-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="e03ed-124">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="e03ed-124">MAPI Structures</span></span>](mapi-structures.md)

