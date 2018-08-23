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
ms.openlocfilehash: 924ddbc7c2ad1ed84ce6927ae089b6eb223bfb92
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563503"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="c2700-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="c2700-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="c2700-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2700-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2700-105">Contém uma matriz de estruturas de **STnefProblem** descrevendo um ou mais processamento problemas que ocorreram durante a codificação ou decodificação de um stream TNEF Transport Neutral Encapsulation Format ().</span><span class="sxs-lookup"><span data-stu-id="c2700-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2700-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c2700-106">Header file:</span></span>  <br/> |<span data-ttu-id="c2700-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="c2700-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="c2700-108">Members</span><span class="sxs-lookup"><span data-stu-id="c2700-108">Members</span></span>

 <span data-ttu-id="c2700-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="c2700-109">**cProblem**</span></span>
  
> <span data-ttu-id="c2700-110">Contagem de elementos na matriz especificada no membro **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="c2700-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="c2700-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="c2700-111">**aProblem**</span></span>
  
> <span data-ttu-id="c2700-112">Matriz de estruturas de [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="c2700-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="c2700-113">Cada estrutura contém informações sobre uma propriedade ou atributo problema de processamento.</span><span class="sxs-lookup"><span data-stu-id="c2700-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c2700-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2700-114">Remarks</span></span>

<span data-ttu-id="c2700-115">Se ocorrer um problema durante o processamento de propriedade ou atributo, um parâmetro de saída no método [ITnef::ExtractProps](itnef-extractprops.md) e do método [ITnef::Finish](itnef-finish.md) receber um ponteiro para uma estrutura **STnefProblemArray** e **ExtractProps **e **Concluir a** cada retornar o valor MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="c2700-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="c2700-116">Esse valor de erro indica que um problema surgiu durante o processamento e uma estrutura de **STnefProblemArray** foi gerada.</span><span class="sxs-lookup"><span data-stu-id="c2700-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="c2700-117">Se uma estrutura de **STnefProblem** não foi gerada durante o processamento de um atributo ou propriedade, o aplicativo cliente pode continuar com a pressuposição de que o processamento desse atributo ou a propriedade teve êxito.</span><span class="sxs-lookup"><span data-stu-id="c2700-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="c2700-118">A única exceção ocorre quando o problema surgiu durante a decodificação de um bloco de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="c2700-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="c2700-119">Se o erro ocorreu durante este decodificação, MAPI_E_UNABLE_TO_COMPLETE pode ser retornado como o [SCODE](scode.md) na estrutura.</span><span class="sxs-lookup"><span data-stu-id="c2700-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="c2700-120">Nesse caso, o componente correspondente para o bloco de decodificação é interrompido e decodificação continua no outro componente.</span><span class="sxs-lookup"><span data-stu-id="c2700-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2700-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2700-121">See also</span></span>



[<span data-ttu-id="c2700-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="c2700-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="c2700-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="c2700-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="c2700-124">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c2700-124">MAPI Structures</span></span>](mapi-structures.md)

