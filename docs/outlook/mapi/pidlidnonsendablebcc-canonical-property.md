---
title: Propriedade canônica PidLidNonSendableBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBcc
api_type:
- COM
ms.assetid: c7523896-c391-443d-bd4e-cc13f3367f08
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7b7cfe1fc1068e5b5b228c4de4c9317d9bcbbc66
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401003"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="fedb4-103">Propriedade canônica PidLidNonSendableBcc</span><span class="sxs-lookup"><span data-stu-id="fedb4-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="fedb4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fedb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fedb4-105">Contém uma lista de todos os participantes outro que são recursos.</span><span class="sxs-lookup"><span data-stu-id="fedb4-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fedb4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fedb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fedb4-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="fedb4-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="fedb4-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="fedb4-108">Property set:</span></span>  <br/> |<span data-ttu-id="fedb4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fedb4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fedb4-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="fedb4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fedb4-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="fedb4-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="fedb4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fedb4-112">Data type:</span></span>  <br/> |<span data-ttu-id="fedb4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fedb4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fedb4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fedb4-114">Area:</span></span>  <br/> |<span data-ttu-id="fedb4-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="fedb4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fedb4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fedb4-116">Remarks</span></span>

<span data-ttu-id="fedb4-117">O valor para cada participante é a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do participante catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="fedb4-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="fedb4-118">Entradas separadas devem ser delimitadas por ponto e vírgula seguido por um espaço.</span><span class="sxs-lookup"><span data-stu-id="fedb4-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="fedb4-119">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="fedb4-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fedb4-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fedb4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fedb4-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fedb4-121">Protocol specifications</span></span>

<span data-ttu-id="fedb4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fedb4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fedb4-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fedb4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fedb4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fedb4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fedb4-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="fedb4-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="fedb4-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fedb4-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fedb4-127">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="fedb4-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fedb4-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fedb4-128">Header files</span></span>

<span data-ttu-id="fedb4-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fedb4-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="fedb4-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fedb4-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fedb4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fedb4-131">See also</span></span>



[<span data-ttu-id="fedb4-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fedb4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fedb4-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fedb4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fedb4-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fedb4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fedb4-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fedb4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

