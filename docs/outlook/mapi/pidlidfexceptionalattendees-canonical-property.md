---
title: Propriedade canônica PidLidFExceptionalAttendees
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7c7f654d42df7856b0e69bf276a763ccd29d1d87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768453"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="49dc7-103">Propriedade canônica PidLidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="49dc7-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="49dc7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49dc7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49dc7-105">Indica se esta propriedade é um objeto calendar recorrente com um ou mais exceções e pelo menos uma das mensagens de exceção incorporada tem pelo menos um RecipientRow.</span><span class="sxs-lookup"><span data-stu-id="49dc7-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49dc7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="49dc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49dc7-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="49dc7-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="49dc7-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="49dc7-108">Property set:</span></span>  <br/> |<span data-ttu-id="49dc7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="49dc7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="49dc7-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="49dc7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="49dc7-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="49dc7-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="49dc7-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="49dc7-112">Data type:</span></span>  <br/> |<span data-ttu-id="49dc7-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="49dc7-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="49dc7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="49dc7-114">Area:</span></span>  <br/> |<span data-ttu-id="49dc7-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="49dc7-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49dc7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="49dc7-116">Remarks</span></span>

<span data-ttu-id="49dc7-117">A ausência dessa propriedade, ou um valor FALSE indica que o objeto calendar tem sem exceções, ou nenhuma das mensagens de exceção incorporada tem RecipientRows.</span><span class="sxs-lookup"><span data-stu-id="49dc7-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49dc7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="49dc7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49dc7-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="49dc7-119">Protocol specifications</span></span>

<span data-ttu-id="49dc7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49dc7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49dc7-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="49dc7-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49dc7-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49dc7-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49dc7-123">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="49dc7-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49dc7-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49dc7-124">Header files</span></span>

<span data-ttu-id="49dc7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49dc7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="49dc7-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="49dc7-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49dc7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="49dc7-127">See also</span></span>



[<span data-ttu-id="49dc7-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="49dc7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49dc7-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="49dc7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49dc7-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="49dc7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49dc7-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="49dc7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

