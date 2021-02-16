---
title: Propriedade canônica PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325617"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="dce10-103">Propriedade canônica PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="dce10-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="dce10-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dce10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dce10-105">Contém TRUE se esse usuário de mensagens é especificamente nomeado como um destinatário primário (Para), cópia carbono (CC) ou cópia carbono (CC) dessa mensagem e não faz parte de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="dce10-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dce10-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dce10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dce10-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="dce10-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="dce10-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dce10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dce10-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="dce10-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="dce10-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dce10-110">Data type:</span></span>  <br/> |<span data-ttu-id="dce10-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dce10-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="dce10-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dce10-112">Area:</span></span>  <br/> |<span data-ttu-id="dce10-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="dce10-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dce10-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dce10-114">Remarks</span></span>

<span data-ttu-id="dce10-115">Essa propriedade fornece uma maneira conveniente de determinar se o nome de usuário aparece explicitamente na lista de destinatários, sem examinar todas as entradas na lista.</span><span class="sxs-lookup"><span data-stu-id="dce10-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="dce10-116">O valor representa a operação **OR** lógica das propriedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) e **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) e as informações de Cc (que, de outra forma, não aparecem em uma propriedade).</span><span class="sxs-lookup"><span data-stu-id="dce10-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="dce10-117">Essa propriedade auxilia o tratamento automatizado de mensagens recebidas no momento do recebimento.</span><span class="sxs-lookup"><span data-stu-id="dce10-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="dce10-118">Na opção do provedor de transporte, essa propriedade conterá FALSE ou não será incluída se o usuário de mensagens não estiver listado diretamente na tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="dce10-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="dce10-119">A entrega de mensagens que resulta da expansão da lista de distribuição não faz com que essa propriedade seja definida.</span><span class="sxs-lookup"><span data-stu-id="dce10-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="dce10-120">O destinatário deve ser explicitamente nomeado.</span><span class="sxs-lookup"><span data-stu-id="dce10-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="dce10-121">Mensagens não enviadas geralmente não configuram essa propriedade, **PR_MESSAGE_CC_ME** ou **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="dce10-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="dce10-122">Se eles estão presentes nas mensagens que o usuário pode acessar em armazenamentos de mensagens públicas, em armazenamentos particulares de outros usuários, em arquivos no disco ou incorporados dentro de outras mensagens recebidas, eles geralmente contêm os valores para os quais foram definidos na última vez que um provedor de transporte entregue a mensagem.</span><span class="sxs-lookup"><span data-stu-id="dce10-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dce10-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dce10-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dce10-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="dce10-124">Protocol specifications</span></span>

<span data-ttu-id="dce10-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dce10-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dce10-126">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dce10-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dce10-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dce10-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dce10-128">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="dce10-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dce10-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="dce10-129">Header files</span></span>

<span data-ttu-id="dce10-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dce10-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="dce10-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dce10-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="dce10-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dce10-132">Mapitags.h</span></span>
  
> <span data-ttu-id="dce10-133">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dce10-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dce10-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dce10-134">See also</span></span>



[<span data-ttu-id="dce10-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dce10-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dce10-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dce10-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dce10-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dce10-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dce10-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dce10-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

