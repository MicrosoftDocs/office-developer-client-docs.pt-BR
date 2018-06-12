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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 8595cdb411e68f2aed3ac063b2b81965e9b4d975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770516"
---
# <a name="stnefproblem"></a><span data-ttu-id="ba08d-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="ba08d-103">STnefProblem</span></span>

  
  
<span data-ttu-id="ba08d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba08d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba08d-105">Contém informações sobre um problema de processamento de propriedade ou atributo que ocorreram durante a codificação ou decodificação de um stream TNEF Transport Neutral Encapsulation Format ().</span><span class="sxs-lookup"><span data-stu-id="ba08d-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba08d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ba08d-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba08d-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="ba08d-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="ba08d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ba08d-108">Members</span></span>

 <span data-ttu-id="ba08d-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="ba08d-109">**ulComponent**</span></span>
  
> <span data-ttu-id="ba08d-110">O tipo de processamento durante o qual o problema ocorreu.</span><span class="sxs-lookup"><span data-stu-id="ba08d-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="ba08d-111">Se o problema ocorreu durante o processamento de mensagens, o membro **ulComponent** é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="ba08d-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="ba08d-112">Se o problema ocorreu durante o processamento de anexo, **ulComponent** é definido igual ao valor de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo correspondente.</span><span class="sxs-lookup"><span data-stu-id="ba08d-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="ba08d-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="ba08d-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="ba08d-114">Atributo associado à propriedade indicada pelo membro **ulPropTag** ou, quando o problema de processamento TNEF ocorre quando um encapsulamento de decodificação bloquear, um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ba08d-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="ba08d-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="ba08d-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="ba08d-116">Nível de mensagem</span><span class="sxs-lookup"><span data-stu-id="ba08d-116">Message level</span></span>
    
 <span data-ttu-id="ba08d-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="ba08d-117">_attAttachment_</span></span>
  
> <span data-ttu-id="ba08d-118">Nível de anexo</span><span class="sxs-lookup"><span data-stu-id="ba08d-118">Attachment level</span></span>
    
 <span data-ttu-id="ba08d-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="ba08d-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="ba08d-120">Marca de propriedade da propriedade que causou o problema de processamento TNEF, exceto quando o problema ocorre quando um bloco de encapsulamento no qual maiusculas **ulPropTag** é definido como zero de decodificação.</span><span class="sxs-lookup"><span data-stu-id="ba08d-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="ba08d-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="ba08d-121">**scode**</span></span>
  
> <span data-ttu-id="ba08d-122">Valor de erro indicando que o problema encontrado durante o processamento.</span><span class="sxs-lookup"><span data-stu-id="ba08d-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba08d-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ba08d-123">Remarks</span></span>

<span data-ttu-id="ba08d-124">Se uma estrutura de **STnefProblem** não foi gerada durante o processamento de um atributo ou propriedade, o aplicativo pode continuar com a pressuposição de que o processamento desse atributo ou a propriedade teve êxito.</span><span class="sxs-lookup"><span data-stu-id="ba08d-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="ba08d-125">A única exceção ocorre quando o problema surgiu durante a decodificação de um bloco de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="ba08d-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="ba08d-126">Nesse caso, o componente correspondente para o bloco de decodificação é interrompido e decodificação continua no outro componente.</span><span class="sxs-lookup"><span data-stu-id="ba08d-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ba08d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba08d-127">See also</span></span>



[<span data-ttu-id="ba08d-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="ba08d-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="ba08d-129">Propriedade canônico de PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="ba08d-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="ba08d-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="ba08d-130">MAPI Structures</span></span>](mapi-structures.md)

