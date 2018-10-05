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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382460"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="19b96-103">Propriedade canônica PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="19b96-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="19b96-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19b96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19b96-105">Conterá TRUE se esse usuário de mensagens é especificamente denominado primário (a), cópia carbono (CC) ou destinatário de cópia oculta (Cco) desta mensagem e não faz parte de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="19b96-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19b96-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="19b96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19b96-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="19b96-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="19b96-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="19b96-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19b96-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="19b96-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="19b96-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="19b96-110">Data type:</span></span>  <br/> |<span data-ttu-id="19b96-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="19b96-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="19b96-112">Área:</span><span class="sxs-lookup"><span data-stu-id="19b96-112">Area:</span></span>  <br/> |<span data-ttu-id="19b96-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="19b96-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19b96-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="19b96-114">Remarks</span></span>

<span data-ttu-id="19b96-115">Essa propriedade oferece uma maneira conveniente para determinar se o nome de usuário aparece explicitamente na lista de destinatários, sem o exame todas as entradas na lista.</span><span class="sxs-lookup"><span data-stu-id="19b96-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="19b96-116">O valor representa a operação **OR** lógica das propriedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) e **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) e as informações de Cco (quais caso contrário, não aparecem em um propriedade).</span><span class="sxs-lookup"><span data-stu-id="19b96-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="19b96-117">Essa propriedade auxilia tratamento automatizado de mensagens recebidas no momento da confirmação.</span><span class="sxs-lookup"><span data-stu-id="19b96-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="19b96-118">Em opção do provedor de transporte, essa propriedade contém FALSE ou não está incluída se o usuário de mensagens não estiver listado diretamente na tabela de destinatário.</span><span class="sxs-lookup"><span data-stu-id="19b96-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="19b96-119">Entrega de mensagem que é resultado da expansão de lista de distribuição não faz com que essa propriedade ser definida.</span><span class="sxs-lookup"><span data-stu-id="19b96-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="19b96-120">O destinatário deve ser nomeado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="19b96-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="19b96-121">As mensagens não enviadas geralmente não definir esta propriedade, **PR_MESSAGE_CC_ME**ou **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="19b96-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="19b96-122">Se eles estiverem presentes em mensagens que o usuário pode acessar em repositórios de mensagem pública, em particular de outros usuários repositórios, nos arquivos em disco, ou incorporado dentro de outras mensagens recebidas, geralmente contêm os valores aos quais foram definidos a última vez que um provedor de transporte entregue a mensagem.</span><span class="sxs-lookup"><span data-stu-id="19b96-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19b96-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="19b96-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19b96-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="19b96-124">Protocol specifications</span></span>

<span data-ttu-id="19b96-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19b96-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19b96-126">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="19b96-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19b96-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19b96-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19b96-128">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="19b96-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19b96-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="19b96-129">Header files</span></span>

<span data-ttu-id="19b96-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19b96-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="19b96-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="19b96-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="19b96-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="19b96-132">Mapitags.h</span></span>
  
> <span data-ttu-id="19b96-133">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="19b96-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19b96-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="19b96-134">See also</span></span>



[<span data-ttu-id="19b96-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="19b96-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19b96-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="19b96-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19b96-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="19b96-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19b96-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="19b96-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

