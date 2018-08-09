---
title: Propriedade canônica PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: be2d30f511540b2eb7aa6e55531753811aaa580d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770108"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="8200d-103">Propriedade canônica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="8200d-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="8200d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8200d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8200d-105">Contém um prefixo de assunto que geralmente indica alguma ação em uma mensagem, como "firmware:" para encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="8200d-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8200d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8200d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8200d-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="8200d-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="8200d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8200d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8200d-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="8200d-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="8200d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8200d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8200d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8200d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8200d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8200d-112">Area:</span></span>  <br/> |<span data-ttu-id="8200d-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="8200d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8200d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8200d-114">Remarks</span></span>

<span data-ttu-id="8200d-115">Essas propriedades são recomendadas em todos os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8200d-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="8200d-116">O prefixo de assunto consiste em um ou mais caracteres alfanuméricos, seguidos por dois pontos e um espaço (que fazem parte do prefixo).</span><span class="sxs-lookup"><span data-stu-id="8200d-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="8200d-117">Ele não deve conter caracteres não alfanuméricos antes dos dois pontos.</span><span class="sxs-lookup"><span data-stu-id="8200d-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="8200d-118">Ausência de um prefixo pode ser representada por uma sequência vazia ou por essa propriedade não está definido.</span><span class="sxs-lookup"><span data-stu-id="8200d-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="8200d-119">Se essas propriedades são definidas explicitamente, a cadeia de caracteres pode ter qualquer comprimento e usar qualquer caractere alfanumérico, mas deve corresponder uma subcadeia de caracteres no início da propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8200d-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="8200d-120">Se essas propriedades não são definidas pelo remetente e devem ser calculadas, seus conteúdos são mais restritos.</span><span class="sxs-lookup"><span data-stu-id="8200d-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="8200d-121">A regra de computação o prefixo é que **PR_SUBJECT** deve começar com um, dois ou três letras (alfabéticos apenas) seguido por dois pontos e um espaço.</span><span class="sxs-lookup"><span data-stu-id="8200d-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="8200d-122">Se uma subcadeia de caracteres for encontrada no início do **PR_SUBJECT**, ele se tornará a cadeia de caracteres para essas propriedades (e também permanece no início do **PR_SUBJECT**).</span><span class="sxs-lookup"><span data-stu-id="8200d-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="8200d-123">Caso contrário, essas propriedades permanecem não definidas.</span><span class="sxs-lookup"><span data-stu-id="8200d-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="8200d-124">Essas propriedades e **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) devem ser calculado como parte da implementação do [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="8200d-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="8200d-125">Um cliente não deve solicitar [IMAPIProp::GetProps](imapiprop-getprops.md) para seus valores até que forem confirmadas por uma chamada **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="8200d-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="8200d-126">As propriedades de assunto são normalmente pequenas cadeias de caracteres de menos de 256 caracteres e um provedor de armazenamento de mensagem não é obrigado a suporte à interface **IStream** do OLE neles.</span><span class="sxs-lookup"><span data-stu-id="8200d-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="8200d-127">Um cliente deve sempre tentar o acesso por meio da interface **IMAPIProp** pela primeira vez e recorrer a **IStream** apenas se **MAPI_E_NOT_ENOUGH_MEMORY** é retornado.</span><span class="sxs-lookup"><span data-stu-id="8200d-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8200d-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8200d-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8200d-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8200d-129">Protocol specifications</span></span>

<span data-ttu-id="8200d-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8200d-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8200d-131">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8200d-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8200d-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8200d-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8200d-133">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="8200d-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8200d-134">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8200d-134">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8200d-135">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8200d-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8200d-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8200d-136">Header files</span></span>

<span data-ttu-id="8200d-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8200d-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="8200d-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8200d-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="8200d-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8200d-139">Mapitags.h</span></span>
  
> <span data-ttu-id="8200d-140">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8200d-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8200d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="8200d-141">See also</span></span>



[<span data-ttu-id="8200d-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8200d-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8200d-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8200d-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8200d-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8200d-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8200d-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8200d-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

