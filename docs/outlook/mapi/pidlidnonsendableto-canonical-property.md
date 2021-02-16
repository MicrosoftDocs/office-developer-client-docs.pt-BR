---
title: Propriedade canônica PidLidNonSendableTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableTo
api_type:
- COM
ms.assetid: 90e14969-652b-422a-9b0a-ee99e58bc8d5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cc510cb9a4a79f977cb6c9721921833441df23c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345512"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="a845a-103">Propriedade canônica PidLidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="a845a-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="a845a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a845a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a845a-105">Contém uma lista de todos os participantes inaendáveis que também são participantes necessários.</span><span class="sxs-lookup"><span data-stu-id="a845a-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a845a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a845a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a845a-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="a845a-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="a845a-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="a845a-108">Property set:</span></span>  <br/> |<span data-ttu-id="a845a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a845a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a845a-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a845a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a845a-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="a845a-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="a845a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a845a-112">Data type:</span></span>  <br/> |<span data-ttu-id="a845a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a845a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a845a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a845a-114">Area:</span></span>  <br/> |<span data-ttu-id="a845a-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="a845a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a845a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a845a-116">Remarks</span></span>

<span data-ttu-id="a845a-117">O valor para cada participante é a **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do Address Book do participante.</span><span class="sxs-lookup"><span data-stu-id="a845a-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="a845a-118">Entradas separadas devem ser delimitadas por um ponto-e-vírgula seguido por um espaço.</span><span class="sxs-lookup"><span data-stu-id="a845a-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="a845a-119">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="a845a-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a845a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a845a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a845a-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a845a-121">Protocol specifications</span></span>

<span data-ttu-id="a845a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a845a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a845a-123">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a845a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a845a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a845a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a845a-125">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="a845a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a845a-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a845a-126">Header files</span></span>

<span data-ttu-id="a845a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a845a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a845a-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a845a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a845a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a845a-129">See also</span></span>



[<span data-ttu-id="a845a-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a845a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a845a-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a845a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a845a-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a845a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a845a-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a845a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

