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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329306"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="a14ec-103">Propriedade canônica PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="a14ec-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="a14ec-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a14ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a14ec-105">Contém TRUE se um remetente da mensagem desejar notificação de não confirmação para um destinatário especificado.</span><span class="sxs-lookup"><span data-stu-id="a14ec-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a14ec-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a14ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a14ec-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="a14ec-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="a14ec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a14ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a14ec-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="a14ec-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="a14ec-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a14ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="a14ec-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a14ec-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a14ec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a14ec-112">Area:</span></span>  <br/> |<span data-ttu-id="a14ec-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="a14ec-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a14ec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a14ec-114">Remarks</span></span>

<span data-ttu-id="a14ec-115">Se essa propriedade contiver FALSE e a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contiver true, o provedor de serviços poderá substituir a propriedade **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** e gerar um notificação de falha na entrega.</span><span class="sxs-lookup"><span data-stu-id="a14ec-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a14ec-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a14ec-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a14ec-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a14ec-117">Header files</span></span>

<span data-ttu-id="a14ec-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a14ec-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="a14ec-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a14ec-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="a14ec-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a14ec-120">Mapitags.h</span></span>
  
> <span data-ttu-id="a14ec-121">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="a14ec-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a14ec-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a14ec-122">See also</span></span>



[<span data-ttu-id="a14ec-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a14ec-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a14ec-124">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a14ec-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a14ec-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a14ec-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a14ec-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a14ec-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

