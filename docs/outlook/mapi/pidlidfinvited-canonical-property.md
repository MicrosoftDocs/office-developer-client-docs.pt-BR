---
title: Propriedade canônica PidLidFInvited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3c2ddb5da9202e9cf0d1c78da1c1ad085ef9687c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386149"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="6104a-103">Propriedade canônica PidLidFInvited</span><span class="sxs-lookup"><span data-stu-id="6104a-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="6104a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6104a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6104a-105">Indica se ou não foram enviados convites para a reunião que representa essa reunião.</span><span class="sxs-lookup"><span data-stu-id="6104a-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6104a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6104a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6104a-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="6104a-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="6104a-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="6104a-108">Property set:</span></span>  <br/> |<span data-ttu-id="6104a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6104a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6104a-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="6104a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6104a-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="6104a-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="6104a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6104a-112">Data type:</span></span>  <br/> |<span data-ttu-id="6104a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6104a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6104a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6104a-114">Area:</span></span>  <br/> |<span data-ttu-id="6104a-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="6104a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6104a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6104a-116">Remarks</span></span>

<span data-ttu-id="6104a-117">A ausência dessa propriedade, ou um valor FALSE indica que uma solicitação de reunião nunca foi enviada.</span><span class="sxs-lookup"><span data-stu-id="6104a-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="6104a-118">Um valor TRUE indica que uma solicitação de reunião foi enviada.</span><span class="sxs-lookup"><span data-stu-id="6104a-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="6104a-119">Depois que esse valor é definido como TRUE em uma reunião, ele não deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="6104a-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6104a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6104a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6104a-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6104a-121">Protocol specifications</span></span>

<span data-ttu-id="6104a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6104a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6104a-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6104a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6104a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6104a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6104a-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="6104a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6104a-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6104a-126">Header files</span></span>

<span data-ttu-id="6104a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6104a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6104a-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6104a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6104a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6104a-129">See also</span></span>



[<span data-ttu-id="6104a-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6104a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6104a-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6104a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6104a-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6104a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6104a-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6104a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

