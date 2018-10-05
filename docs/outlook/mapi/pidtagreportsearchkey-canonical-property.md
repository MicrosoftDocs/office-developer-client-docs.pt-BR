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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383503"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="38f44-103">Propriedade canônica PidTagReportSearchKey</span><span class="sxs-lookup"><span data-stu-id="38f44-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="38f44-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38f44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38f44-105">Contém a chave de pesquisa para o destinatário que deve obter relatórios para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="38f44-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38f44-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="38f44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38f44-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="38f44-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="38f44-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="38f44-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38f44-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="38f44-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="38f44-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="38f44-110">Data type:</span></span>  <br/> |<span data-ttu-id="38f44-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="38f44-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="38f44-112">Área:</span><span class="sxs-lookup"><span data-stu-id="38f44-112">Area:</span></span>  <br/> |<span data-ttu-id="38f44-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="38f44-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38f44-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38f44-114">Remarks</span></span>

<span data-ttu-id="38f44-115">Essa propriedade é uma das propriedades de endereço do destinatário que o remetente tenha delegada para receber qualquer relatórios gerados para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="38f44-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="38f44-116">Um aplicativo cliente que deve rotear relatórios para outro usuário deverá definir essa propriedade em tempo de envio de mensagem.</span><span class="sxs-lookup"><span data-stu-id="38f44-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="38f44-117">Se não estiver definida, os relatórios são enviados para o remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="38f44-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38f44-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="38f44-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38f44-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="38f44-119">Protocol specifications</span></span>

<span data-ttu-id="38f44-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38f44-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38f44-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="38f44-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38f44-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38f44-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38f44-123">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="38f44-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38f44-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="38f44-124">Header files</span></span>

<span data-ttu-id="38f44-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38f44-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="38f44-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="38f44-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="38f44-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="38f44-127">Mapitags.h</span></span>
  
> <span data-ttu-id="38f44-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="38f44-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38f44-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="38f44-129">See also</span></span>



[<span data-ttu-id="38f44-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="38f44-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38f44-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="38f44-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38f44-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="38f44-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38f44-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="38f44-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

