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
ms.openlocfilehash: b5bc464bc5a251579d262f5926193b7f7a731728
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563655"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="25c3a-103">Propriedade canônica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="25c3a-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="25c3a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25c3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25c3a-105">Contém o assunto da mensagem com nenhum prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="25c3a-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25c3a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="25c3a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25c3a-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="25c3a-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="25c3a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="25c3a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25c3a-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="25c3a-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="25c3a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="25c3a-110">Data type:</span></span>  <br/> |<span data-ttu-id="25c3a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25c3a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="25c3a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="25c3a-112">Area:</span></span>  <br/> |<span data-ttu-id="25c3a-113">Email</span><span class="sxs-lookup"><span data-stu-id="25c3a-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25c3a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="25c3a-114">Remarks</span></span>

<span data-ttu-id="25c3a-115">Essas propriedades são computadas pelo armazenamento de mensagens ou transportam provedores do **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e propriedades de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="25c3a-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="25c3a-116">Se o **PR_SUBJECT_PREFIX** estiver presente e uma subcadeia inicial **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** e propriedades associadas estão definidas para o conteúdo de **PR_SUBJECT** com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="25c3a-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="25c3a-117">Se **PR_SUBJECT_PREFIX** estiver presente, mas não é uma subcadeia inicial **PR_SUBJECT**, **PR_SUBJECT_PREFIX** é excluída e recalculado a partir **PR_SUBJECT** usando a seguinte regra: se a cadeia de caracteres contida no **PR_SUBJECT** começa com um a três caracteres de não-numérico seguidos por dois pontos e um espaço, a cadeia de caracteres em conjunto com os dois pontos e o valor em branco se tornará o prefixo.</span><span class="sxs-lookup"><span data-stu-id="25c3a-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="25c3a-118">Números, espaços em branco e caracteres de pontuação não são caracteres de prefixo válido.</span><span class="sxs-lookup"><span data-stu-id="25c3a-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="25c3a-119">Se **PR_SUBJECT_PREFIX** não estiver presente, é calculada a partir **PR_SUBJECT** usando a regra descrita na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="25c3a-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="25c3a-120">Essa propriedade, em seguida, é definida como o conteúdo de **PR_SUBJECT** com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="25c3a-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="25c3a-121">**Observação** Quando **PR_SUBJECT_PREFIX** é uma sequência vazia, **PR_SUBJECT** e essa propriedade são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="25c3a-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="25c3a-122">Por fim, esta propriedade deve ser a parte da **PR_SUBJECT** seguindo o prefixo.</span><span class="sxs-lookup"><span data-stu-id="25c3a-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="25c3a-123">Se não houver nenhum prefixo, essa propriedade se torna a mesma **PR_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="25c3a-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="25c3a-124">**PR_SUBJECT_PREFIX** e esta propriedade devem ser calculados como parte da implementação do [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="25c3a-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="25c3a-125">Um aplicativo cliente não deve solicitar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para seus valores até que forem confirmadas por uma chamada **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="25c3a-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="25c3a-126">As propriedades de assunto são normalmente pequenas cadeias de caracteres de menos de 256 caracteres e um provedor de armazenamento de mensagem não é obrigado a oferecer suporte a interface de vinculação e incorporação de objetos (OLE) **IStream** neles.</span><span class="sxs-lookup"><span data-stu-id="25c3a-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="25c3a-127">O cliente deve sempre tentar o acesso por meio da interface **IMAPIProp** pela primeira vez e recorrer a **IStream** apenas se MAPI_E_NOT_ENOUGH_MEMORY é retornado.</span><span class="sxs-lookup"><span data-stu-id="25c3a-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25c3a-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="25c3a-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25c3a-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="25c3a-129">Protocol specifications</span></span>

<span data-ttu-id="25c3a-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25c3a-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25c3a-131">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="25c3a-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25c3a-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25c3a-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25c3a-133">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="25c3a-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="25c3a-134">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25c3a-134">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25c3a-135">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="25c3a-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25c3a-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="25c3a-136">Header files</span></span>

<span data-ttu-id="25c3a-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25c3a-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="25c3a-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="25c3a-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="25c3a-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="25c3a-139">Mapitags.h</span></span>
  
> <span data-ttu-id="25c3a-140">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="25c3a-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25c3a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="25c3a-141">See also</span></span>



[<span data-ttu-id="25c3a-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="25c3a-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25c3a-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="25c3a-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25c3a-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="25c3a-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25c3a-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="25c3a-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

