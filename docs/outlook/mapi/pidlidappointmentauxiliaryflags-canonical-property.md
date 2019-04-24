---
title: Propriedade canônica PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345427"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="d6b08-103">Propriedade canônica PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="d6b08-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d6b08-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6b08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6b08-105">Especifica um campo de bits que descreve o estado auxiliar do objeto.</span><span class="sxs-lookup"><span data-stu-id="d6b08-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6b08-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d6b08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6b08-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="d6b08-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="d6b08-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="d6b08-108">Property set:</span></span>  <br/> |<span data-ttu-id="d6b08-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d6b08-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d6b08-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d6b08-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d6b08-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="d6b08-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="d6b08-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d6b08-112">Data type:</span></span>  <br/> |<span data-ttu-id="d6b08-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d6b08-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d6b08-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d6b08-114">Area:</span></span>  <br/> |<span data-ttu-id="d6b08-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="d6b08-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6b08-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6b08-116">Remarks</span></span>

<span data-ttu-id="d6b08-117">Esta propriedade não é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="d6b08-117">This property is not required.</span></span> <span data-ttu-id="d6b08-118">Veja a seguir os sinalizadores individuais que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="d6b08-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="d6b08-119">C (auxApptFlagCopied, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d6b08-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="d6b08-120">Este sinalizador indica que o objeto Calendar foi copiado de outra pasta de calendário.</span><span class="sxs-lookup"><span data-stu-id="d6b08-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="d6b08-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d6b08-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="d6b08-122">Esse sinalizador em uma solicitação de reunião indica que o cliente ou servidor deve enviar uma resposta de reunião de volta para o organizador quando uma resposta for escolhida.</span><span class="sxs-lookup"><span data-stu-id="d6b08-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="d6b08-123">F (auxApptFlagForwarded, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="d6b08-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="d6b08-124">Esse sinalizador em uma solicitação de reunião indica que ela foi encaminhada (incluindo ser encaminhada pelo organizador), em vez de ser um convite do organizador.</span><span class="sxs-lookup"><span data-stu-id="d6b08-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d6b08-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6b08-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6b08-126">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="d6b08-126">Protocol specifications</span></span>

<span data-ttu-id="d6b08-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6b08-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6b08-128">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d6b08-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6b08-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6b08-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6b08-130">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="d6b08-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6b08-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d6b08-131">Header files</span></span>

<span data-ttu-id="d6b08-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d6b08-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6b08-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d6b08-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6b08-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6b08-134">See also</span></span>



[<span data-ttu-id="d6b08-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b08-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6b08-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b08-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6b08-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b08-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6b08-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d6b08-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

