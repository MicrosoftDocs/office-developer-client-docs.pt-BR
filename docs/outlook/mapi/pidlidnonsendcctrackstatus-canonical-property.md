---
title: Propriedade canônica PidLidNonSendCcTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319667"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="5cb3e-103">Propriedade canônica PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="5cb3e-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="5cb3e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5cb3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5cb3e-105">Contém o valor de cada participante listado na **propriedade dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5cb3e-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5cb3e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5cb3e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5cb3e-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="5cb3e-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="5cb3e-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="5cb3e-108">Property set:</span></span>  <br/> |<span data-ttu-id="5cb3e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5cb3e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5cb3e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5cb3e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5cb3e-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="5cb3e-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="5cb3e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5cb3e-112">Data type:</span></span>  <br/> |<span data-ttu-id="5cb3e-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="5cb3e-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="5cb3e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5cb3e-114">Area:</span></span>  <br/> |<span data-ttu-id="5cb3e-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="5cb3e-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cb3e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cb3e-116">Remarks</span></span>

<span data-ttu-id="5cb3e-117">Essa propriedade é necessária somente quando a **propriedade dispidNonSendableCC** está definida.</span><span class="sxs-lookup"><span data-stu-id="5cb3e-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="5cb3e-118">O número de valores nesta propriedade deve ser igual ao número de valores em **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="5cb3e-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="5cb3e-119">Cada PT_LONG valor nessa propriedade corresponde ao participante na **propriedade dispidNonSendableCC** no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="5cb3e-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5cb3e-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cb3e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5cb3e-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5cb3e-121">Protocol specifications</span></span>

<span data-ttu-id="5cb3e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cb3e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cb3e-123">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5cb3e-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5cb3e-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5cb3e-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5cb3e-125">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="5cb3e-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5cb3e-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="5cb3e-126">Header files</span></span>

<span data-ttu-id="5cb3e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5cb3e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5cb3e-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5cb3e-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5cb3e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cb3e-129">See also</span></span>



[<span data-ttu-id="5cb3e-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5cb3e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5cb3e-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5cb3e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5cb3e-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5cb3e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5cb3e-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5cb3e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

