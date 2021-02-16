---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435177"
---
# <a name="stnefproblem"></a><span data-ttu-id="58c67-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="58c67-103">STnefProblem</span></span>

  
  
<span data-ttu-id="58c67-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58c67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58c67-105">Contém informações sobre um problema de processamento de propriedade ou atributo que ocorreu durante a codificação ou decodificação de um fluxo TNEF (Transport Neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="58c67-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58c67-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="58c67-106">Header file:</span></span>  <br/> |<span data-ttu-id="58c67-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="58c67-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="58c67-108">Members</span><span class="sxs-lookup"><span data-stu-id="58c67-108">Members</span></span>

 <span data-ttu-id="58c67-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="58c67-109">**ulComponent**</span></span>
  
> <span data-ttu-id="58c67-110">O tipo de processamento durante o qual o problema ocorreu.</span><span class="sxs-lookup"><span data-stu-id="58c67-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="58c67-111">Se o problema ocorreu durante o processamento de mensagens, o **membro ulComponent** é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="58c67-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="58c67-112">Se o problema ocorreu durante o processamento do anexo, **ulComponent** é definido como o valor **de PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) correspondente.</span><span class="sxs-lookup"><span data-stu-id="58c67-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="58c67-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="58c67-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="58c67-114">Atributo associado à propriedade indicada pelo membro **ulPropTag** ou, quando o problema de processamento TNEF ocorre ao decodificar um bloco de encapsulamento, um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="58c67-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="58c67-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="58c67-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="58c67-116">Nível da mensagem</span><span class="sxs-lookup"><span data-stu-id="58c67-116">Message level</span></span>
    
 <span data-ttu-id="58c67-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="58c67-117">_attAttachment_</span></span>
  
> <span data-ttu-id="58c67-118">Nível de anexo</span><span class="sxs-lookup"><span data-stu-id="58c67-118">Attachment level</span></span>
    
 <span data-ttu-id="58c67-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="58c67-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="58c67-120">Marca de propriedade da propriedade que causou o problema de processamento TNEF, exceto quando o problema ocorre ao decodificar um bloco de encapsulamento; nesse caso, **ulPropTag** é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="58c67-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="58c67-121">**scode**</span><span class="sxs-lookup"><span data-stu-id="58c67-121">**scode**</span></span>
  
> <span data-ttu-id="58c67-122">Valor de erro indicando o problema encontrado durante o processamento.</span><span class="sxs-lookup"><span data-stu-id="58c67-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58c67-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="58c67-123">Remarks</span></span>

<span data-ttu-id="58c67-124">Se uma **estrutura STnefProblem** não for gerada durante o processamento de um atributo ou propriedade, o aplicativo poderá continuar pressupor que o processamento desse atributo ou propriedade foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="58c67-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="58c67-125">A única exceção ocorre quando o problema surge durante a decodificação de um bloco de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="58c67-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="58c67-126">Nesse caso, a decodificação do componente correspondente ao bloco é interrompida e a decodificação continua em outro componente.</span><span class="sxs-lookup"><span data-stu-id="58c67-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58c67-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="58c67-127">See also</span></span>



[<span data-ttu-id="58c67-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="58c67-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="58c67-129">Propriedade canônica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="58c67-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="58c67-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="58c67-130">MAPI Structures</span></span>](mapi-structures.md)

