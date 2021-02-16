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
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339225"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="ff847-103">Propriedade canônica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="ff847-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="ff847-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff847-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff847-105">Contém um prefixo de assunto que normalmente indica alguma ação em uma mensagem, como "FW: " para encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="ff847-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff847-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ff847-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff847-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="ff847-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="ff847-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ff847-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff847-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="ff847-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="ff847-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ff847-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff847-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff847-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ff847-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ff847-112">Area:</span></span>  <br/> |<span data-ttu-id="ff847-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="ff847-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff847-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff847-114">Remarks</span></span>

<span data-ttu-id="ff847-115">Essas propriedades são recomendadas em todos os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ff847-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="ff847-116">O prefixo de assunto consiste em um ou mais caracteres alfanuméricos, seguidos por dois-pontos e um espaço (que fazem parte do prefixo).</span><span class="sxs-lookup"><span data-stu-id="ff847-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="ff847-117">Ele não deve conter caracteres não-cônicos antes dos dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="ff847-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="ff847-118">A ausência de um prefixo pode ser representada por uma cadeia de caracteres vazia ou por essa propriedade não estar sendo definida.</span><span class="sxs-lookup"><span data-stu-id="ff847-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="ff847-119">Se essas propriedades são definidas explicitamente, a cadeia de caracteres pode ser de qualquer comprimento e usar quaisquer caracteres alfanuméricos, mas deve corresponder a uma substring no início da propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ff847-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="ff847-120">Se essas propriedades não são definidas pelo remetente e devem ser computadas, seu conteúdo é mais restrito.</span><span class="sxs-lookup"><span data-stu-id="ff847-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="ff847-121">A regra para calcular o prefixo **é PR_SUBJECT** deve começar com uma, duas ou três letras (somente alfabéticas) seguidas por dois-pontos e um espaço.</span><span class="sxs-lookup"><span data-stu-id="ff847-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="ff847-122">Se tal substring for encontrada no início de **PR_SUBJECT**, ela se tornará a cadeia de caracteres para essas propriedades (e também permanecerá no início de PR_SUBJECT **).**</span><span class="sxs-lookup"><span data-stu-id="ff847-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="ff847-123">Caso contrário, essas propriedades permanecerão não ativas.</span><span class="sxs-lookup"><span data-stu-id="ff847-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="ff847-124">Essas propriedades e **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) devem ser computadas como parte da implementação [de IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="ff847-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="ff847-125">Um cliente não deve solicitar [a IMAPIProp::GetProps](imapiprop-getprops.md) seus valores até que eles tenham sido confirmados por uma chamada **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="ff847-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="ff847-126">As propriedades de assunto são normalmente pequenas cadeias de caracteres com menos de 256 caracteres, e um provedor de armazenamento de mensagens não é obrigado a dar suporte à interface **OLE IStream** neles.</span><span class="sxs-lookup"><span data-stu-id="ff847-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="ff847-127">Um cliente deve sempre tentar acessar pela interface **IMAPIProp** primeiro e recorrer a **IStream** somente **se** MAPI_E_NOT_ENOUGH_MEMORY for retornado.</span><span class="sxs-lookup"><span data-stu-id="ff847-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ff847-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff847-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff847-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ff847-129">Protocol specifications</span></span>

<span data-ttu-id="ff847-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff847-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff847-131">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ff847-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff847-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff847-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff847-133">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="ff847-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ff847-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff847-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff847-135">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="ff847-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff847-136">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ff847-136">Header files</span></span>

<span data-ttu-id="ff847-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff847-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff847-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ff847-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff847-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff847-139">Mapitags.h</span></span>
  
> <span data-ttu-id="ff847-140">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ff847-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff847-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff847-141">See also</span></span>



[<span data-ttu-id="ff847-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ff847-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff847-143">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ff847-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff847-144">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ff847-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff847-145">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ff847-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

