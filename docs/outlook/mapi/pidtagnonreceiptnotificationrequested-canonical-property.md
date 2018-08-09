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
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769513"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="9cd2a-103">Propriedade canônica PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="9cd2a-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="9cd2a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9cd2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9cd2a-105">Contém TRUE se o remetente da mensagem Maria notificação de não-recebimento por um destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="9cd2a-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9cd2a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9cd2a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cd2a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="9cd2a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="9cd2a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9cd2a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9cd2a-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="9cd2a-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="9cd2a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9cd2a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9cd2a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9cd2a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9cd2a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9cd2a-112">Area:</span></span>  <br/> |<span data-ttu-id="9cd2a-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="9cd2a-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cd2a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cd2a-114">Remarks</span></span>

<span data-ttu-id="9cd2a-115">Se essa propriedade contém FALSE e a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) conterá TRUE, o provedor de serviços pode substituir a propriedade **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** e gerar um relatório de falha na entrega.</span><span class="sxs-lookup"><span data-stu-id="9cd2a-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9cd2a-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cd2a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9cd2a-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9cd2a-117">Header files</span></span>

<span data-ttu-id="9cd2a-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cd2a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cd2a-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9cd2a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="9cd2a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9cd2a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="9cd2a-121">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="9cd2a-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cd2a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cd2a-122">See also</span></span>



[<span data-ttu-id="9cd2a-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9cd2a-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cd2a-124">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9cd2a-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cd2a-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9cd2a-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cd2a-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9cd2a-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

