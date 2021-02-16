---
title: Propriedade canônica PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329733"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="fc0ee-103">Propriedade canônica PidTagMessageCcMe</span><span class="sxs-lookup"><span data-stu-id="fc0ee-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="fc0ee-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc0ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc0ee-105">Contém TRUE se esse usuário de mensagens é especificamente nomeado como um destinatário de cópia carbono (CC) dessa mensagem e não faz parte de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc0ee-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fc0ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc0ee-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="fc0ee-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="fc0ee-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc0ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc0ee-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="fc0ee-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="fc0ee-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fc0ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc0ee-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fc0ee-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fc0ee-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc0ee-112">Area:</span></span>  <br/> |<span data-ttu-id="fc0ee-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="fc0ee-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc0ee-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc0ee-114">Remarks</span></span>

<span data-ttu-id="fc0ee-115">Essa propriedade fornece uma maneira conveniente de determinar se o nome de usuário aparece explicitamente na lista de destinatários de cópia carbono, sem examinar todas as entradas na lista.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="fc0ee-116">Essa propriedade também auxilia o tratamento automatizado de mensagens recebidas no momento do recebimento.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="fc0ee-117">Na opção do provedor de transporte, essa propriedade conterá FALSE ou não será definida se o usuário de mensagens não estiver listado diretamente na tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="fc0ee-118">A entrega de mensagens resultante da expansão da lista de distribuição ou de uma designação de cópia carbono não faz com que essa propriedade seja definida.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="fc0ee-119">O destinatário deve ser explicitamente nomeado.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="fc0ee-120">Mensagens não enviadas geralmente não configuram essa propriedade, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fc0ee-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="fc0ee-121">Se eles estão presentes nas mensagens que o usuário pode acessar em armazenamentos de mensagens públicas, em armazenamentos particulares de outros usuários, em arquivos no disco ou incorporados em outras mensagens recebidas, eles geralmente contêm os valores para os quais foram definidos na última vez que um provedor de transporte entregue a mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc0ee-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc0ee-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc0ee-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fc0ee-123">Protocol specifications</span></span>

<span data-ttu-id="fc0ee-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc0ee-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc0ee-125">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc0ee-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc0ee-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc0ee-127">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc0ee-128">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="fc0ee-128">Header files</span></span>

<span data-ttu-id="fc0ee-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc0ee-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc0ee-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc0ee-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc0ee-131">Mapitags.h</span></span>
  
> <span data-ttu-id="fc0ee-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fc0ee-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc0ee-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc0ee-133">See also</span></span>



[<span data-ttu-id="fc0ee-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc0ee-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc0ee-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fc0ee-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc0ee-136">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fc0ee-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc0ee-137">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fc0ee-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

