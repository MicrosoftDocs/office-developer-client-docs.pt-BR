---
title: Propriedade canônica PidLidFExceptionalBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327458"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="0feb4-103">Propriedade canônica PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="0feb4-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="0feb4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0feb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0feb4-105">Indica que o objeto de mensagem incorporada da exceção tem um corpo diferente do objeto de calendário recorrente.</span><span class="sxs-lookup"><span data-stu-id="0feb4-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0feb4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0feb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0feb4-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="0feb4-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="0feb4-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="0feb4-108">Property set:</span></span>  <br/> |<span data-ttu-id="0feb4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0feb4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0feb4-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0feb4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0feb4-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="0feb4-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="0feb4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0feb4-112">Data type:</span></span>  <br/> |<span data-ttu-id="0feb4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0feb4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0feb4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0feb4-114">Area:</span></span>  <br/> |<span data-ttu-id="0feb4-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="0feb4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0feb4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0feb4-116">Remarks</span></span>

<span data-ttu-id="0feb4-117">Se o valor dessa propriedade for VERDADEIRO, o objeto de mensagem incorporada de exceção deverá ter um corpo.</span><span class="sxs-lookup"><span data-stu-id="0feb4-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="0feb4-118">Se o valor dessa propriedade for FALSO ou se a propriedade não existir, um cliente ou servidor deverá obter o corpo do objeto de calendário recorrente.</span><span class="sxs-lookup"><span data-stu-id="0feb4-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0feb4-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0feb4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0feb4-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0feb4-120">Protocol specifications</span></span>

<span data-ttu-id="0feb4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0feb4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0feb4-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0feb4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0feb4-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0feb4-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0feb4-124">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="0feb4-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0feb4-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="0feb4-125">Header files</span></span>

<span data-ttu-id="0feb4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0feb4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0feb4-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0feb4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0feb4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0feb4-128">See also</span></span>



[<span data-ttu-id="0feb4-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0feb4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0feb4-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0feb4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0feb4-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0feb4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0feb4-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0feb4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

