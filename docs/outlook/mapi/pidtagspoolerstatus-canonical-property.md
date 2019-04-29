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
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408674"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="d6cc7-103">Propriedade canônica PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="d6cc7-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="d6cc7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6cc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6cc7-105">Contém o status da mensagem com base nas informações que estão disponíveis para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6cc7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d6cc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6cc7-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="d6cc7-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="d6cc7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d6cc7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6cc7-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="d6cc7-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="d6cc7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d6cc7-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6cc7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d6cc7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d6cc7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d6cc7-112">Area:</span></span>  <br/> |<span data-ttu-id="d6cc7-113">MAPI não-transmittable</span><span class="sxs-lookup"><span data-stu-id="d6cc7-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6cc7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6cc7-114">Remarks</span></span>

<span data-ttu-id="d6cc7-115">Esta propriedade é calculada por MAPI em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="d6cc7-116">Essa propriedade aparece somente em mensagens de entrada e é reservada em todos os outros casos.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="d6cc7-117">Ele indica se uma mensagem foi entregue ou não ao seu local final ou se um provedor de conexão de mensagens possivelmente excluiu a mensagem ao reroteá-la.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="d6cc7-118">Os aplicativos cliente nunca devem definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-118">Client applications should never set this property.</span></span> <span data-ttu-id="d6cc7-119">Para uma mensagem de entrada, um cliente ou um provedor de serviços pode chamar [IMAPIProp::](imapiprop-getprops.md) GetProps nessa propriedade para determinar o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="d6cc7-120">O valor S_OK indica que a mensagem foi entregue com êxito ao repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="d6cc7-121">O valor MAPI_E_OBJECT_DELETED indica que a mensagem foi excluída e nunca foi confirmada no repositório.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="d6cc7-122">Os provedores de repositório de mensagens devem oferecer suporte a essa propriedade em mensagens, tabelas de destinatários e na tabela de fila de saída.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="d6cc7-123">Os clientes e provedores devem ser capazes de definir colunas na tabela de fila de saída e restringir com base nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d6cc7-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6cc7-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d6cc7-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d6cc7-125">Header files</span></span>

<span data-ttu-id="d6cc7-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d6cc7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6cc7-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6cc7-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d6cc7-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d6cc7-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d6cc7-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6cc7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6cc7-130">See also</span></span>



[<span data-ttu-id="d6cc7-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6cc7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6cc7-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d6cc7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6cc7-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d6cc7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6cc7-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d6cc7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

