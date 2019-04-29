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
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435275"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="49492-103">Propriedade canônica PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="49492-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="49492-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49492-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49492-105">Contém a data e hora da entrega da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="49492-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49492-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="49492-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49492-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="49492-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="49492-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="49492-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49492-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="49492-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="49492-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="49492-110">Data type:</span></span>  <br/> |<span data-ttu-id="49492-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="49492-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="49492-112">Área:</span><span class="sxs-lookup"><span data-stu-id="49492-112">Area:</span></span>  <br/> |<span data-ttu-id="49492-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="49492-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49492-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="49492-114">Remarks</span></span>

<span data-ttu-id="49492-115">Esta propriedade é uma propriedade por destinatário em um relatório de entrega que indica o momento em que a mensagem original foi entregue ao usuário de mensagens para o qual o relatório de entrega está sendo gerado.</span><span class="sxs-lookup"><span data-stu-id="49492-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49492-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="49492-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="49492-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49492-117">Header files</span></span>

<span data-ttu-id="49492-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="49492-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="49492-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="49492-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="49492-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="49492-120">Mapitags.h</span></span>
  
> <span data-ttu-id="49492-121">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="49492-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49492-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="49492-122">See also</span></span>



[<span data-ttu-id="49492-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="49492-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="49492-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="49492-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49492-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="49492-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49492-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="49492-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49492-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="49492-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

