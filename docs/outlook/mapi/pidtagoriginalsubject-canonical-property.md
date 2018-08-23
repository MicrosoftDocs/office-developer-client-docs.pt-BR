---
title: Propriedade canônica PidTagOriginalSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b49398b822e6972a8a6d02e1dff9c2316ce6eb33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566632"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="11416-103">Propriedade canônica PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="11416-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="11416-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11416-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11416-105">Contém o assunto de uma mensagem original para uso em um relatório sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="11416-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11416-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="11416-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11416-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="11416-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="11416-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="11416-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11416-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="11416-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="11416-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="11416-110">Data type:</span></span>  <br/> |<span data-ttu-id="11416-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11416-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="11416-112">Área:</span><span class="sxs-lookup"><span data-stu-id="11416-112">Area:</span></span>  <br/> |<span data-ttu-id="11416-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="11416-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11416-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="11416-114">Remarks</span></span>

<span data-ttu-id="11416-115">Essas propriedades originalmente são definidas para o mesmo valor que a propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11416-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="11416-116">As propriedades de assunto são normalmente pequenas cadeias de caracteres de menos de 256 caracteres e um provedor de armazenamento de mensagem não é obrigado a oferecer suporte a interface de vinculação e incorporação de objetos (OLE) **IStream** neles.</span><span class="sxs-lookup"><span data-stu-id="11416-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="11416-117">O cliente deve sempre tentar o acesso por meio da interface **IMAPIProp** pela primeira vez e recorrer a **IStream** apenas se **MAPI_E_NOT_ENOUGH_MEMORY** é retornado.</span><span class="sxs-lookup"><span data-stu-id="11416-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="11416-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="11416-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11416-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="11416-119">Protocol specifications</span></span>

<span data-ttu-id="11416-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11416-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11416-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="11416-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11416-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11416-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11416-123">Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="11416-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="11416-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11416-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11416-125">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="11416-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11416-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="11416-126">Header files</span></span>

<span data-ttu-id="11416-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11416-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="11416-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="11416-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="11416-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11416-129">Mapitags.h</span></span>
  
> <span data-ttu-id="11416-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="11416-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11416-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="11416-131">See also</span></span>



[<span data-ttu-id="11416-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="11416-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11416-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="11416-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11416-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="11416-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11416-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="11416-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

