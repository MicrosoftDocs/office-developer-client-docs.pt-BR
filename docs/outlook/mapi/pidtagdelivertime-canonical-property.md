---
title: Propriedade canônica PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 198e388f5cfb6ab0431e7b7a78b9a0be3d103597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582116"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="7014a-103">Propriedade canônica PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="7014a-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="7014a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7014a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7014a-105">Contém a data e hora de quando a mensagem original foi entregue.</span><span class="sxs-lookup"><span data-stu-id="7014a-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7014a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7014a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7014a-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="7014a-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="7014a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7014a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7014a-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="7014a-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="7014a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7014a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7014a-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7014a-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7014a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7014a-112">Area:</span></span>  <br/> |<span data-ttu-id="7014a-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="7014a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7014a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7014a-114">Remarks</span></span>

<span data-ttu-id="7014a-115">Essa propriedade é uma propriedade por destinatário em um relatório de entrega que indica a hora em que a mensagem original foi entregue ao usuário mensagens para o qual o relatório de entrega está sendo gerado.</span><span class="sxs-lookup"><span data-stu-id="7014a-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7014a-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7014a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7014a-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7014a-117">Header files</span></span>

<span data-ttu-id="7014a-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7014a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="7014a-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7014a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="7014a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7014a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="7014a-121">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7014a-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7014a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7014a-122">See also</span></span>



[<span data-ttu-id="7014a-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="7014a-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="7014a-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7014a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7014a-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7014a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7014a-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7014a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7014a-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7014a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

