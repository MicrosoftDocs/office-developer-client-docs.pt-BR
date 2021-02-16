---
title: Propriedade canônica PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329271"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="1f961-103">Propriedade canônica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="1f961-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="1f961-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f961-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f961-105">Contém o assunto da mensagem com qualquer prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="1f961-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f961-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1f961-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f961-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="1f961-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="1f961-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1f961-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f961-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="1f961-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="1f961-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f961-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f961-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f961-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1f961-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1f961-112">Area:</span></span>  <br/> |<span data-ttu-id="1f961-113">Email</span><span class="sxs-lookup"><span data-stu-id="1f961-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f961-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f961-114">Remarks</span></span>

<span data-ttu-id="1f961-115">Essas propriedades são calculadas pelo armazenamento de mensagens ou por provedores de transporte das propriedades **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="1f961-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="1f961-116">Se o **PR_SUBJECT_PREFIX** estiver presente e for uma substring inicial de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** e as propriedades associadas serão definidas para o conteúdo de **PR_SUBJECT** com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="1f961-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="1f961-117">Se **PR_SUBJECT_PREFIX** estiver presente, mas não for uma substring inicial de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** será excluído e recalculado de PR_SUBJECT usando **PR_SUBJECT** seguinte regra: se a cadeia de caracteres contida em PR_SUBJECT começar com um **a** três caracteres não numéricos seguidos por dois pontos e um espaço, a cadeia de caracteres juntamente com os dois pontos e o vazio se tornará o prefixo.</span><span class="sxs-lookup"><span data-stu-id="1f961-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="1f961-118">Números, espaços em branco e caracteres de pontuação não são caracteres de prefixo válidos.</span><span class="sxs-lookup"><span data-stu-id="1f961-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="1f961-119">Se **PR_SUBJECT_PREFIX** não estiver presente, ele será calculado a partir **PR_SUBJECT** a regra descrita na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="1f961-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="1f961-120">Em seguida, essa propriedade é definida para o conteúdo **da PR_SUBJECT** com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="1f961-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="1f961-121">**Observação** Quando **PR_SUBJECT_PREFIX** é uma cadeia de caracteres vazia, **PR_SUBJECT** e essa propriedade são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="1f961-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="1f961-122">Por fim, essa propriedade deve ser a parte **PR_SUBJECT** seguir o prefixo.</span><span class="sxs-lookup"><span data-stu-id="1f961-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="1f961-123">Se não houver prefixo, essa propriedade se tornará a mesma que **PR_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="1f961-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="1f961-124">**PR_SUBJECT_PREFIX** e essa propriedade devem ser calculadas como parte da implementação [de IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="1f961-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="1f961-125">Um aplicativo cliente não deve solicitar ao método [IMAPIProp::GetProps](imapiprop-getprops.md) seus valores até que eles tenham sido confirmados por uma chamada **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="1f961-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="1f961-126">As propriedades de assunto são normalmente pequenas cadeias de caracteres com menos de 256 caracteres, e um provedor de armazenamento de mensagens não é obrigado a dar suporte à interface **IStream** de vinculação e incorporação de objetos (OLE) neles.</span><span class="sxs-lookup"><span data-stu-id="1f961-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="1f961-127">O cliente deve sempre tentar acessar pela interface **IMAPIProp** primeiro e recorrer a **IStream** somente se MAPI_E_NOT_ENOUGH_MEMORY for retornado.</span><span class="sxs-lookup"><span data-stu-id="1f961-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f961-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f961-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f961-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1f961-129">Protocol specifications</span></span>

<span data-ttu-id="1f961-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f961-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f961-131">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f961-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f961-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f961-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f961-133">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="1f961-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="1f961-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f961-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f961-135">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="1f961-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f961-136">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1f961-136">Header files</span></span>

<span data-ttu-id="1f961-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f961-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f961-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1f961-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f961-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f961-139">Mapitags.h</span></span>
  
> <span data-ttu-id="1f961-140">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1f961-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f961-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f961-141">See also</span></span>



[<span data-ttu-id="1f961-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1f961-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f961-143">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1f961-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f961-144">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1f961-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f961-145">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1f961-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

