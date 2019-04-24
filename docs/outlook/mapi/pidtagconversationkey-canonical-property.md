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
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334696"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="5a238-103">Propriedade canônica PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="5a238-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="5a238-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a238-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a238-105">Contém a chave de conversa usada no Microsoft Outlook somente ao localizar \*\*IPM. \*\*Mensagens de MessageManager, como a mensagem que contém o histórico de download de uma conta POP3 (Post Office Protocol).</span><span class="sxs-lookup"><span data-stu-id="5a238-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="5a238-106">Essa propriedade foi preterida no Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5a238-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a238-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5a238-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a238-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="5a238-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="5a238-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5a238-109">Identifier:</span></span>  <br/> |<span data-ttu-id="5a238-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="5a238-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="5a238-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5a238-111">Data type:</span></span>  <br/> |<span data-ttu-id="5a238-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a238-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a238-113">Área:</span><span class="sxs-lookup"><span data-stu-id="5a238-113">Area:</span></span>  <br/> |<span data-ttu-id="5a238-114">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="5a238-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a238-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a238-115">Remarks</span></span>

<span data-ttu-id="5a238-116">Ao acessar mensagens de email como conversas e converter Propriedades de mensagens no [formato de encapsulamento de transporte neutro (TNEF)](transport-neutral-encapsulation-format-tnef.md), não use essa propriedade; em vez disso, use as propriedades canônicas [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) e [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="5a238-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5a238-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a238-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a238-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="5a238-118">Protocol specifications</span></span>

<span data-ttu-id="5a238-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a238-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a238-120">Fornece referências para as especificações de protocolo do Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5a238-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a238-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a238-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a238-122">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="5a238-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="5a238-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a238-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a238-124">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="5a238-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a238-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5a238-125">Header files</span></span>

<span data-ttu-id="5a238-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5a238-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a238-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5a238-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a238-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5a238-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5a238-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5a238-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a238-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a238-130">See also</span></span>



[<span data-ttu-id="5a238-131">SubÁrvore IPM</span><span class="sxs-lookup"><span data-stu-id="5a238-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="5a238-132">Pastas especiais MAPI</span><span class="sxs-lookup"><span data-stu-id="5a238-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="5a238-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a238-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a238-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5a238-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a238-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5a238-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a238-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5a238-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

