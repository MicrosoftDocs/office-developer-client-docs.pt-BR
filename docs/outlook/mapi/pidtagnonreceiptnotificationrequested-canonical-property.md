---
title: Propriedade canônica PidTagNonReceiptNotificationRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419748"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="2ba04-103">Propriedade canônica PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="2ba04-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="2ba04-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ba04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ba04-105">Contém TRUE se um remetente de mensagem deseja notificação de não recebimento para um destinatário especificado.</span><span class="sxs-lookup"><span data-stu-id="2ba04-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ba04-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2ba04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ba04-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="2ba04-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="2ba04-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2ba04-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ba04-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="2ba04-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="2ba04-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2ba04-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ba04-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2ba04-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2ba04-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2ba04-112">Area:</span></span>  <br/> |<span data-ttu-id="2ba04-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="2ba04-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ba04-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ba04-114">Remarks</span></span>

<span data-ttu-id="2ba04-115">Se essa propriedade contiver FALSE e a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contiver TRUE, o provedor de serviços poderá substituir a propriedade **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** e gerar um relatório de não entrega.</span><span class="sxs-lookup"><span data-stu-id="2ba04-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ba04-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ba04-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2ba04-117">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="2ba04-117">Header files</span></span>

<span data-ttu-id="2ba04-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ba04-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ba04-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2ba04-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ba04-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ba04-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2ba04-121">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="2ba04-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ba04-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ba04-122">See also</span></span>



[<span data-ttu-id="2ba04-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2ba04-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ba04-124">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2ba04-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ba04-125">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2ba04-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ba04-126">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2ba04-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

