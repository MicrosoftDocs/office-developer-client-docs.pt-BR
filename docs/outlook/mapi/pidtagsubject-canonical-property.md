---
title: Propriedade canônica PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 63bb5534756f44aebd9e6ca21c336534b279909d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770103"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="00fc0-103">Propriedade canônica PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="00fc0-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="00fc0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00fc0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00fc0-105">Contém o assunto completo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="00fc0-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00fc0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="00fc0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00fc0-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="00fc0-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="00fc0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="00fc0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00fc0-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="00fc0-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="00fc0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="00fc0-110">Data type:</span></span>  <br/> |<span data-ttu-id="00fc0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00fc0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="00fc0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="00fc0-112">Area:</span></span>  <br/> |<span data-ttu-id="00fc0-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="00fc0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00fc0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="00fc0-114">Remarks</span></span>

<span data-ttu-id="00fc0-115">Essas propriedades são recomendadas em todos os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="00fc0-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="00fc0-116">Essas propriedades são sempre o texto do assunto completo, ou seja, a concatenação do prefixo e o assunto normalizado.</span><span class="sxs-lookup"><span data-stu-id="00fc0-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="00fc0-117">Se não houver nenhum prefixo, o assunto normalizado deve ser o mesmo que o assunto.</span><span class="sxs-lookup"><span data-stu-id="00fc0-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="00fc0-118">Uma mensagem armazenar ou essas propriedades e propriedades de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) para calcular o assunto normalizado usando a regra descritas em **PR_NORMALIZED_SUBJECT** ([ de usos de provedor de transporte PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="00fc0-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="00fc0-119">As propriedades de assunto são normalmente pequenas cadeias de caracteres de menos de 256 caracteres e um provedor de armazenamento de mensagem não é obrigado a suporte à interface **IStream** neles.</span><span class="sxs-lookup"><span data-stu-id="00fc0-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="00fc0-120">O cliente deve sempre tentar o acesso por meio da interface **IMAPIProp** pela primeira vez e recorrer a **IStream** apenas se **MAPI_E_NOT_ENOUGH_MEMORY** é retornado.</span><span class="sxs-lookup"><span data-stu-id="00fc0-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="00fc0-121">Para um relatório, essa propriedade contém o assunto da mensagem original precedido por uma cadeia de caracteres indicando o que aconteceu com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="00fc0-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="00fc0-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="00fc0-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00fc0-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="00fc0-123">Protocol specifications</span></span>

<span data-ttu-id="00fc0-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00fc0-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00fc0-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="00fc0-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00fc0-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00fc0-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00fc0-127">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="00fc0-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00fc0-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="00fc0-128">Header files</span></span>

<span data-ttu-id="00fc0-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00fc0-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="00fc0-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="00fc0-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="00fc0-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00fc0-131">Mapitags.h</span></span>
  
> <span data-ttu-id="00fc0-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="00fc0-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00fc0-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="00fc0-133">See also</span></span>



[<span data-ttu-id="00fc0-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="00fc0-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00fc0-135">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="00fc0-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00fc0-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="00fc0-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00fc0-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="00fc0-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

