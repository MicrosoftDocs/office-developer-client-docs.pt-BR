---
title: Propriedade canônica PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d04144a4f5ef714b59b608bfe19367bcb3c1ced8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588570"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="96deb-103">Propriedade canônica PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="96deb-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="96deb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96deb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96deb-105">Contém o status da mensagem com base nas informações que está disponíveis para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="96deb-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96deb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="96deb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96deb-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="96deb-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="96deb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="96deb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96deb-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="96deb-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="96deb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="96deb-110">Data type:</span></span>  <br/> |<span data-ttu-id="96deb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="96deb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="96deb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="96deb-112">Area:</span></span>  <br/> |<span data-ttu-id="96deb-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="96deb-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96deb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="96deb-114">Remarks</span></span>

<span data-ttu-id="96deb-115">Essa propriedade é computada pelo MAPI em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="96deb-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="96deb-116">Essa propriedade é exibida no somente mensagens de entrada e está reservada em todos os outros casos.</span><span class="sxs-lookup"><span data-stu-id="96deb-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="96deb-117">Indica se uma mensagem foi entregue ao local final ou se um provedor de fora do gancho mensagens potencialmente excluiu a mensagem enquanto reencaminhamento-lo.</span><span class="sxs-lookup"><span data-stu-id="96deb-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="96deb-118">Aplicativos cliente nunca devem definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="96deb-118">Client applications should never set this property.</span></span> <span data-ttu-id="96deb-119">Para uma mensagem de entrada, um provedor de cliente ou serviço pode chamar [IMAPIProp::GetProps](imapiprop-getprops.md) sobre esta propriedade para determinar o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="96deb-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="96deb-120">O valor S_OK indica que a mensagem foi entregue com êxito para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="96deb-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="96deb-121">O valor MAPI_E_OBJECT_DELETED indica que a mensagem foi excluída e nunca foi comprometida com o repositório.</span><span class="sxs-lookup"><span data-stu-id="96deb-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="96deb-122">Provedores de armazenamento de mensagem devem oferecer suporte a essa propriedade em mensagens, tabelas de destinatários e a tabela de fila de saída.</span><span class="sxs-lookup"><span data-stu-id="96deb-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="96deb-123">Clientes e provedores devem poder definir colunas na tabela de fila de saída e restringir com base nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="96deb-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="96deb-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="96deb-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="96deb-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96deb-125">Header files</span></span>

<span data-ttu-id="96deb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96deb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="96deb-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="96deb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="96deb-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96deb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="96deb-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="96deb-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96deb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="96deb-130">See also</span></span>



[<span data-ttu-id="96deb-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="96deb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96deb-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="96deb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96deb-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="96deb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96deb-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="96deb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

