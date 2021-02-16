---
title: Propriedade canônica PidTagReportSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 889b43bb606cbe9c96d52c8a21ffda5dfcebb1da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359175"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="dae68-103">Propriedade canônica PidTagReportSearchKey</span><span class="sxs-lookup"><span data-stu-id="dae68-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="dae68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dae68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dae68-105">Contém a chave de pesquisa para o destinatário que deve obter relatórios para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="dae68-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dae68-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dae68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dae68-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="dae68-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="dae68-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dae68-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dae68-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="dae68-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="dae68-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dae68-110">Data type:</span></span>  <br/> |<span data-ttu-id="dae68-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dae68-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dae68-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dae68-112">Area:</span></span>  <br/> |<span data-ttu-id="dae68-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="dae68-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dae68-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dae68-114">Remarks</span></span>

<span data-ttu-id="dae68-115">Essa propriedade é uma das propriedades de endereço do destinatário que o remetente delegou para receber relatórios gerados para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="dae68-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="dae68-116">Um aplicativo cliente que deve rotear relatórios para outro usuário deve definir essa propriedade no momento do envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="dae68-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="dae68-117">Se não estiver definido, os relatórios serão enviados para o remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="dae68-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dae68-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dae68-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dae68-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="dae68-119">Protocol specifications</span></span>

<span data-ttu-id="dae68-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dae68-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dae68-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dae68-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dae68-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dae68-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dae68-123">Especifica as propriedades e operações permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="dae68-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dae68-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="dae68-124">Header files</span></span>

<span data-ttu-id="dae68-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dae68-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dae68-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dae68-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="dae68-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dae68-127">Mapitags.h</span></span>
  
> <span data-ttu-id="dae68-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dae68-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dae68-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dae68-129">See also</span></span>



[<span data-ttu-id="dae68-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dae68-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dae68-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dae68-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dae68-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dae68-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dae68-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dae68-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

