---
title: Propriedade canônica PidTagReportEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 558a2235f7cb617bf37ccff77ebeec6e4ba77604
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582613"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="1261d-103">Propriedade canônica PidTagReportEntryId</span><span class="sxs-lookup"><span data-stu-id="1261d-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1261d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1261d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1261d-105">Contém o identificador de entrada para o destinatário que deve receber relatórios para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="1261d-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1261d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1261d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1261d-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1261d-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1261d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1261d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1261d-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="1261d-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="1261d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1261d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1261d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1261d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1261d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1261d-112">Area:</span></span>  <br/> |<span data-ttu-id="1261d-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="1261d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1261d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1261d-114">Remarks</span></span>

<span data-ttu-id="1261d-115">Essa propriedade é uma das propriedades de endereço do destinatário que o remetente tenha delegada para receber qualquer relatórios gerados para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="1261d-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="1261d-116">Um aplicativo cliente que deve rotear relatórios para outro usuário deverá definir essa propriedade em tempo de envio de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1261d-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="1261d-117">Se não estiver definida, os relatórios são enviados para o remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1261d-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1261d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1261d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1261d-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1261d-119">Protocol specifications</span></span>

<span data-ttu-id="1261d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1261d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1261d-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1261d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1261d-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1261d-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1261d-123">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="1261d-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1261d-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1261d-124">Header files</span></span>

<span data-ttu-id="1261d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1261d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1261d-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1261d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1261d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1261d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1261d-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1261d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1261d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1261d-129">See also</span></span>



[<span data-ttu-id="1261d-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1261d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1261d-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1261d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1261d-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1261d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1261d-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1261d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

