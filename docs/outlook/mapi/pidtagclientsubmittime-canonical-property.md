---
title: Propriedade canônica PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345714"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="400b5-103">Propriedade canônica PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="400b5-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="400b5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="400b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="400b5-105">Contém a data e a hora em que o remetente da mensagem enviou uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="400b5-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="400b5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="400b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="400b5-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="400b5-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="400b5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="400b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="400b5-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="400b5-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="400b5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="400b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="400b5-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="400b5-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="400b5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="400b5-112">Area:</span></span>  <br/> |<span data-ttu-id="400b5-113">Hora da mensagem</span><span class="sxs-lookup"><span data-stu-id="400b5-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="400b5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="400b5-114">Remarks</span></span>

<span data-ttu-id="400b5-115">O provedor da loja **PR_CLIENT_SUBMIT_TIME** o horário em que o aplicativo cliente chamou [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="400b5-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="400b5-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="400b5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="400b5-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="400b5-117">Protocol specifications</span></span>

<span data-ttu-id="400b5-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="400b5-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="400b5-119">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="400b5-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="400b5-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="400b5-120">Header files</span></span>

<span data-ttu-id="400b5-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="400b5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="400b5-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="400b5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="400b5-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="400b5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="400b5-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="400b5-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="400b5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="400b5-125">See also</span></span>



[<span data-ttu-id="400b5-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="400b5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="400b5-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="400b5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="400b5-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="400b5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="400b5-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="400b5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

