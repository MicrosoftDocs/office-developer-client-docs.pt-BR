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
ms.openlocfilehash: 96a0b010a8ba26a0c1b0cb409f1aaabb308a1c01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356193"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="d72e2-103">Propriedade canônica PidTagMessageToMe</span><span class="sxs-lookup"><span data-stu-id="d72e2-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="d72e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d72e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d72e2-105">Contém TRUE se esse usuário de mensagens é especificamente chamado de destinatário principal (para) desta mensagem e não faz parte de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="d72e2-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d72e2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d72e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d72e2-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="d72e2-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="d72e2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d72e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d72e2-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="d72e2-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="d72e2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d72e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="d72e2-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d72e2-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d72e2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d72e2-112">Area:</span></span>  <br/> |<span data-ttu-id="d72e2-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="d72e2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d72e2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d72e2-114">Remarks</span></span>

<span data-ttu-id="d72e2-115">Essa propriedade oferece uma maneira conveniente de determinar se o nome de usuário aparece explicitamente na lista de destinatários principal, sem examinar todas as entradas na lista.</span><span class="sxs-lookup"><span data-stu-id="d72e2-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="d72e2-116">Essa propriedade também auxilia a manipulação automatizada de mensagens recebidas no momento da confirmação.</span><span class="sxs-lookup"><span data-stu-id="d72e2-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="d72e2-117">Na opção do provedor de transporte, essa propriedade conterá FALSE ou não será incluída se o usuário de mensagens não estiver listado diretamente na tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="d72e2-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="d72e2-118">A entrega de mensagens resultante da expansão da lista de distribuição ou de uma designação de cópia oculta não faz com que essa propriedade seja definida.</span><span class="sxs-lookup"><span data-stu-id="d72e2-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="d72e2-119">O destinatário deve ser nomeado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="d72e2-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="d72e2-120">As mensagens não enviadas geralmente não definem o **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), o **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="d72e2-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="d72e2-121">Se estiverem presentes nas mensagens que o usuário pode acessar em repositórios de mensagens públicas, em repositórios privados de outros usuários, em arquivos no disco ou incorporado dentro de outras mensagens recebidas, eles geralmente contêm os valores para os quais foram definidos na última vez que um provedor de transporte entregue a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d72e2-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d72e2-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d72e2-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d72e2-123">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="d72e2-123">Protocol specifications</span></span>

<span data-ttu-id="d72e2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d72e2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d72e2-125">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d72e2-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d72e2-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d72e2-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d72e2-127">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d72e2-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d72e2-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d72e2-128">Header files</span></span>

<span data-ttu-id="d72e2-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d72e2-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="d72e2-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d72e2-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="d72e2-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d72e2-131">Mapitags.h</span></span>
  
> <span data-ttu-id="d72e2-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d72e2-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d72e2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d72e2-133">See also</span></span>



[<span data-ttu-id="d72e2-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d72e2-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d72e2-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d72e2-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d72e2-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d72e2-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d72e2-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d72e2-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

