---
title: Propriedade canônica PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fc9a64abefb9a4acaa9a1da396fb27f897f04ec2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585602"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="c0c22-103">Propriedade canônica PidTagReplyRecipientNames</span><span class="sxs-lookup"><span data-stu-id="c0c22-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="c0c22-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0c22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0c22-105">Contém uma lista de nomes de exibição dos destinatários que devem receber uma resposta.</span><span class="sxs-lookup"><span data-stu-id="c0c22-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0c22-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c0c22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0c22-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="c0c22-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="c0c22-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c0c22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0c22-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="c0c22-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="c0c22-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c0c22-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0c22-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c0c22-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c0c22-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c0c22-112">Area:</span></span>  <br/> |<span data-ttu-id="c0c22-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c22-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0c22-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0c22-114">Remarks</span></span>

<span data-ttu-id="c0c22-115">Essas propriedades contenham os nomes de exibição separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="c0c22-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="c0c22-116">Quando essa propriedade não estiver presente, uma resposta é enviada apenas para o usuário identificado pela propriedade **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c0c22-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="c0c22-117">Quando essas propriedades e **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) são definidas, a resposta é enviada para todos os destinatários identificados por essas duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0c22-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="c0c22-118">Um provedor de transporte usa essas propriedades para substituir a lógica de resposta comum.</span><span class="sxs-lookup"><span data-stu-id="c0c22-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="c0c22-119">Se **PR_REPLY_RECIPIENT_ENTRIES** ou essas propriedades estiverem definidas, a outra propriedade deve ser definida também.</span><span class="sxs-lookup"><span data-stu-id="c0c22-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="c0c22-120">Essas propriedades devem conter o mesmo número de destinatários, e eles devem armazená-los na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="c0c22-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="c0c22-121">Falha para observar esses requisitos pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="c0c22-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c0c22-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0c22-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0c22-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c0c22-123">Protocol specifications</span></span>

<span data-ttu-id="c0c22-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0c22-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0c22-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c0c22-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0c22-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0c22-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0c22-127">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="c0c22-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="c0c22-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0c22-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0c22-129">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0c22-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0c22-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c0c22-130">Header files</span></span>

<span data-ttu-id="c0c22-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0c22-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0c22-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c0c22-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0c22-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c0c22-133">Mapitags.h</span></span>
  
> <span data-ttu-id="c0c22-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c0c22-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0c22-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0c22-135">See also</span></span>



[<span data-ttu-id="c0c22-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c22-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0c22-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c0c22-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0c22-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c0c22-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0c22-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c0c22-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

