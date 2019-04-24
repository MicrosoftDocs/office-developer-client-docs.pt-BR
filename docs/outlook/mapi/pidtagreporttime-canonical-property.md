---
title: Propriedade canônica PidTagReportTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 298c53e537819f800a3acc5cf07c01a7b9f978ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330146"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="951b5-103">Propriedade canônica PidTagReportTime</span><span class="sxs-lookup"><span data-stu-id="951b5-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="951b5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="951b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="951b5-105">Contém a data e hora em que o sistema de mensagens gerou um relatório.</span><span class="sxs-lookup"><span data-stu-id="951b5-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="951b5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="951b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="951b5-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="951b5-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="951b5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="951b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="951b5-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="951b5-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="951b5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="951b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="951b5-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="951b5-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="951b5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="951b5-112">Area:</span></span>  <br/> |<span data-ttu-id="951b5-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="951b5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="951b5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="951b5-114">Remarks</span></span>

<span data-ttu-id="951b5-115">Esta propriedade representa uma propriedade por destinatário em relatórios de entrega e de não entrega e uma propriedade por mensagem em relatórios de leitura e não leitura.</span><span class="sxs-lookup"><span data-stu-id="951b5-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="951b5-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="951b5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="951b5-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="951b5-117">Protocol specifications</span></span>

<span data-ttu-id="951b5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="951b5-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="951b5-119">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="951b5-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="951b5-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="951b5-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="951b5-121">Especifica as propriedades e as operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="951b5-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="951b5-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="951b5-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="951b5-123">Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="951b5-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="951b5-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="951b5-124">Header files</span></span>

<span data-ttu-id="951b5-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="951b5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="951b5-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="951b5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="951b5-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="951b5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="951b5-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="951b5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="951b5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="951b5-129">See also</span></span>



[<span data-ttu-id="951b5-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="951b5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="951b5-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="951b5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="951b5-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="951b5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="951b5-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="951b5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

