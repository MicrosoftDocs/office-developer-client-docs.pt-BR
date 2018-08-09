---
title: Propriedade canônica PidTagMessageToMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 42aec7a8d617bdf1abd385add30d903efa2b73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769490"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="425ac-103">Propriedade canônica PidTagMessageToMe</span><span class="sxs-lookup"><span data-stu-id="425ac-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="425ac-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="425ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="425ac-105">Conterá TRUE se esse usuário de mensagens é especificamente denominado primário (destinatário da mensagem para) e não faz parte de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="425ac-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="425ac-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="425ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="425ac-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="425ac-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="425ac-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="425ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="425ac-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="425ac-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="425ac-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="425ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="425ac-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="425ac-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="425ac-112">Área:</span><span class="sxs-lookup"><span data-stu-id="425ac-112">Area:</span></span>  <br/> |<span data-ttu-id="425ac-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="425ac-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="425ac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="425ac-114">Remarks</span></span>

<span data-ttu-id="425ac-115">Essa propriedade oferece uma maneira conveniente para determinar se o nome de usuário aparece explicitamente na lista de destinatários principal, sem o exame todas as entradas na lista.</span><span class="sxs-lookup"><span data-stu-id="425ac-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="425ac-116">Essa propriedade também contribuem para o tratamento automatizado de mensagens recebidas no momento da confirmação.</span><span class="sxs-lookup"><span data-stu-id="425ac-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="425ac-117">Em opção do provedor de transporte, essa propriedade contém FALSE ou não está incluída se o usuário de mensagens não estiver listado diretamente na tabela de destinatário.</span><span class="sxs-lookup"><span data-stu-id="425ac-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="425ac-118">Entrega de mensagem resultante da expansão de lista de distribuição ou uma designação de cópia oculta não faz com que essa propriedade ser definida.</span><span class="sxs-lookup"><span data-stu-id="425ac-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="425ac-119">O destinatário deve ser nomeado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="425ac-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="425ac-120">As mensagens não enviadas geralmente não definir essa propriedade, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="425ac-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="425ac-121">Se eles estiverem presentes em mensagens que o usuário pode acessar em repositórios de mensagem pública, em particular de outros usuários repositórios, nos arquivos em disco, ou incorporado dentro de outras mensagens recebidas, geralmente contêm os valores aos quais foram definidos a última vez que um provedor de transporte entregue a mensagem.</span><span class="sxs-lookup"><span data-stu-id="425ac-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="425ac-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="425ac-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="425ac-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="425ac-123">Protocol specifications</span></span>

<span data-ttu-id="425ac-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="425ac-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="425ac-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="425ac-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="425ac-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="425ac-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="425ac-127">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="425ac-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="425ac-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="425ac-128">Header files</span></span>

<span data-ttu-id="425ac-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="425ac-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="425ac-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="425ac-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="425ac-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="425ac-131">Mapitags.h</span></span>
  
> <span data-ttu-id="425ac-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="425ac-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="425ac-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="425ac-133">See also</span></span>



[<span data-ttu-id="425ac-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="425ac-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="425ac-135">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="425ac-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="425ac-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="425ac-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="425ac-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="425ac-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

