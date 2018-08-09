---
title: Propriedade canônica PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4aec52497e02e99423fa50f378cd35dbf366c37c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769125"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="e9355-103">Propriedade canônica PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="e9355-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="e9355-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9355-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9355-105">Contém a chave de conversa usada no Microsoft Outlook somente quando localizar **IPM. MessageManager** mensagens, como a mensagem que contém o histórico de download para uma conta de Post Office Protocol (POP3).</span><span class="sxs-lookup"><span data-stu-id="e9355-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="e9355-106">Esta propriedade foi preterida no Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e9355-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9355-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e9355-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9355-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="e9355-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="e9355-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e9355-109">Identifier:</span></span>  <br/> |<span data-ttu-id="e9355-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="e9355-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="e9355-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e9355-111">Data type:</span></span>  <br/> |<span data-ttu-id="e9355-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9355-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9355-113">Área:</span><span class="sxs-lookup"><span data-stu-id="e9355-113">Area:</span></span>  <br/> |<span data-ttu-id="e9355-114">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="e9355-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9355-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9355-115">Remarks</span></span>

<span data-ttu-id="e9355-116">Ao acessar mensagens de email como conversas e converter propriedades da mensagem [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), não use essa propriedade; em vez disso, use as propriedades de canônico [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) e [Mapipidtagconversationtopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="e9355-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9355-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9355-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9355-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e9355-118">Protocol specifications</span></span>

<span data-ttu-id="e9355-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9355-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9355-120">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e9355-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9355-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9355-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9355-122">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e9355-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="e9355-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9355-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9355-124">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="e9355-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9355-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e9355-125">Header files</span></span>

<span data-ttu-id="e9355-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9355-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9355-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e9355-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9355-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9355-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e9355-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e9355-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9355-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9355-130">See also</span></span>



[<span data-ttu-id="e9355-131">Subárvore IPM</span><span class="sxs-lookup"><span data-stu-id="e9355-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="e9355-132">Pastas especiais de MAPI</span><span class="sxs-lookup"><span data-stu-id="e9355-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="e9355-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e9355-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9355-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e9355-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9355-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e9355-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9355-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e9355-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

