---
title: Propriedade canônica PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355052"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="2a878-103">Propriedade canônica PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="2a878-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="2a878-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a878-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a878-105">Contém uma matriz dimensionada de identificadores de entrada para destinatários que receberão uma resposta.</span><span class="sxs-lookup"><span data-stu-id="2a878-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a878-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2a878-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a878-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="2a878-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="2a878-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2a878-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a878-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="2a878-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="2a878-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2a878-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a878-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a878-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a878-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2a878-112">Area:</span></span>  <br/> |<span data-ttu-id="2a878-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="2a878-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a878-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a878-114">Remarks</span></span>

<span data-ttu-id="2a878-115">Essa propriedade contém uma [estrutura FLATENTRYLIST](flatentrylist.md) e não é uma propriedade de múltiplos valores.</span><span class="sxs-lookup"><span data-stu-id="2a878-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="2a878-116">Quando essa propriedade não está presente, uma resposta é enviada apenas para o usuário identificado pela propriedade **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2a878-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="2a878-117">Quando essa e as **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) são definidas, a resposta é enviada a todos os destinatários identificados por essas duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2a878-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="2a878-118">Um provedor de transporte usa essas propriedades para substituir a lógica de resposta comum.</span><span class="sxs-lookup"><span data-stu-id="2a878-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="2a878-119">Se essa propriedade ou a **propriedade PR_REPLY_RECIPIENT_NAMES** estiver definida, a outra propriedade deverá ser definida também.</span><span class="sxs-lookup"><span data-stu-id="2a878-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="2a878-120">Essas propriedades devem conter o mesmo número de destinatários e devem contê-los na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="2a878-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="2a878-121">A falha ao observar esses requisitos pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="2a878-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2a878-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a878-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a878-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2a878-123">Protocol specifications</span></span>

<span data-ttu-id="2a878-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a878-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a878-125">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2a878-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a878-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a878-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a878-127">Especifica as propriedades e operações permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="2a878-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="2a878-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a878-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a878-129">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2a878-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a878-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="2a878-130">Header files</span></span>

<span data-ttu-id="2a878-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a878-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a878-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2a878-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a878-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2a878-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2a878-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2a878-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a878-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a878-135">See also</span></span>



[<span data-ttu-id="2a878-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2a878-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a878-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2a878-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a878-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2a878-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a878-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2a878-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

