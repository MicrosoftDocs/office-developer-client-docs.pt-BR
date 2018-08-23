---
title: Propriedade canônica PidLidAppointmentMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4b26266e58a201b13aa178534039c9e07c900de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569495"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="c79d6-103">Propriedade canônica PidLidAppointmentMessageClass</span><span class="sxs-lookup"><span data-stu-id="c79d6-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="c79d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c79d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c79d6-105">Indica a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da reunião que deve ser geradas a partir da solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="c79d6-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c79d6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c79d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c79d6-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="c79d6-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="c79d6-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="c79d6-108">Property set:</span></span>  <br/> |<span data-ttu-id="c79d6-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="c79d6-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="c79d6-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="c79d6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c79d6-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="c79d6-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="c79d6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c79d6-112">Data type:</span></span>  <br/> |<span data-ttu-id="c79d6-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="c79d6-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="c79d6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c79d6-114">Area:</span></span>  <br/> |<span data-ttu-id="c79d6-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="c79d6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c79d6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c79d6-116">Remarks</span></span>

<span data-ttu-id="c79d6-117">O valor dessa propriedade deve ser "IPM. Compromisso"ou ser prefixados com"IPM. Compromisso. ".</span><span class="sxs-lookup"><span data-stu-id="c79d6-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="c79d6-118">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="c79d6-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c79d6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c79d6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c79d6-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c79d6-120">Protocol specifications</span></span>

<span data-ttu-id="c79d6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c79d6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c79d6-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c79d6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c79d6-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c79d6-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c79d6-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="c79d6-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c79d6-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c79d6-125">Header files</span></span>

<span data-ttu-id="c79d6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c79d6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c79d6-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c79d6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c79d6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c79d6-128">See also</span></span>



[<span data-ttu-id="c79d6-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c79d6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c79d6-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c79d6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c79d6-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c79d6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c79d6-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c79d6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

