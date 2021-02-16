---
title: Propriedade canônica PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334682"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="007ab-103">Propriedade canônica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="007ab-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="007ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="007ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="007ab-105">Contém o tópico da primeira mensagem em um thread de conversa.</span><span class="sxs-lookup"><span data-stu-id="007ab-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="007ab-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="007ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="007ab-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="007ab-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="007ab-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="007ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="007ab-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="007ab-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="007ab-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="007ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="007ab-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="007ab-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="007ab-112">Área:</span><span class="sxs-lookup"><span data-stu-id="007ab-112">Area:</span></span>  <br/> |<span data-ttu-id="007ab-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="007ab-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="007ab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="007ab-114">Remarks</span></span>

<span data-ttu-id="007ab-115">Um thread de conversa representa uma série de mensagens e respostas.</span><span class="sxs-lookup"><span data-stu-id="007ab-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="007ab-116">Essas propriedades são definidas para a primeira mensagem em um thread, geralmente para a propriedade **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="007ab-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="007ab-117">As mensagens subsequentes no thread devem usar o mesmo tópico sem modificação.</span><span class="sxs-lookup"><span data-stu-id="007ab-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="007ab-118">A **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indica a relação de ordem entre mensagens e respostas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="007ab-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="007ab-119">Seu uso é opcional, mesmo que essas propriedades sejam definidas.</span><span class="sxs-lookup"><span data-stu-id="007ab-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="007ab-120">Um provedor de armazenamento de mensagens tem a opção de garante que essas propriedades sejam sempre definidas em mensagens de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="007ab-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="007ab-121">Se essas propriedades já estão definidas, elas não devem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="007ab-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="007ab-122">Caso não, eles podem ser definidos **como PR_NORMALIZED_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="007ab-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="007ab-123">Qualquer ação deve ser tomada antes [que IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="007ab-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="007ab-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="007ab-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="007ab-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="007ab-125">Protocol specifications</span></span>

<span data-ttu-id="007ab-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007ab-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007ab-127">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="007ab-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="007ab-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007ab-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007ab-129">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="007ab-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="007ab-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="007ab-130">Header files</span></span>

<span data-ttu-id="007ab-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="007ab-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="007ab-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="007ab-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="007ab-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="007ab-133">Mapitags.h</span></span>
  
> <span data-ttu-id="007ab-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="007ab-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="007ab-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="007ab-135">See also</span></span>



[<span data-ttu-id="007ab-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="007ab-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="007ab-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="007ab-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="007ab-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="007ab-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="007ab-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="007ab-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

