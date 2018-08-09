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
ms.openlocfilehash: 2e656679fcf76992ec0b648274bd5ffa673b4007
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769128"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="a794d-103">Propriedade canônica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="a794d-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="a794d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a794d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a794d-105">Contém o tópico da primeira mensagem em um segmento de conversação.</span><span class="sxs-lookup"><span data-stu-id="a794d-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a794d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a794d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a794d-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="a794d-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="a794d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a794d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a794d-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="a794d-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="a794d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a794d-110">Data type:</span></span>  <br/> |<span data-ttu-id="a794d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a794d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a794d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a794d-112">Area:</span></span>  <br/> |<span data-ttu-id="a794d-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="a794d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a794d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a794d-114">Remarks</span></span>

<span data-ttu-id="a794d-115">Um thread de conversação representa uma série de mensagens e respostas.</span><span class="sxs-lookup"><span data-stu-id="a794d-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="a794d-116">Essas propriedades são definidas para a primeira mensagem em um segmento, geralmente à propriedade **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a794d-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="a794d-117">Mensagens subsequentes no segmento devem usar o mesmo tópico sem modificação.</span><span class="sxs-lookup"><span data-stu-id="a794d-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="a794d-118">A propriedade **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indica que a relação de ordem entre as mensagens subsequentes e respostas.</span><span class="sxs-lookup"><span data-stu-id="a794d-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="a794d-119">Seu uso é opcional, mesmo se essas propriedades serão definidas.</span><span class="sxs-lookup"><span data-stu-id="a794d-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="a794d-120">Um provedor de armazenamento de mensagem tem a opção de assegurar que essas propriedades são sempre definidas em mensagens de entrada ou saídas.</span><span class="sxs-lookup"><span data-stu-id="a794d-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="a794d-121">Se essas propriedades já estiverem definidas eles não devem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="a794d-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="a794d-122">Caso contrário, elas podem ser definidas para **PR_NORMALIZED_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="a794d-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="a794d-123">Qualquer ação deve ser executada antes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="a794d-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a794d-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a794d-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a794d-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a794d-125">Protocol specifications</span></span>

<span data-ttu-id="a794d-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a794d-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a794d-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a794d-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a794d-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a794d-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a794d-129">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a794d-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a794d-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a794d-130">Header files</span></span>

<span data-ttu-id="a794d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a794d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a794d-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a794d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a794d-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a794d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a794d-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a794d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a794d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a794d-135">See also</span></span>



[<span data-ttu-id="a794d-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a794d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a794d-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a794d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a794d-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a794d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a794d-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a794d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

