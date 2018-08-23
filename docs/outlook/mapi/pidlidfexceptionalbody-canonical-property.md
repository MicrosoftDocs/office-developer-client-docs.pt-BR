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
ms.openlocfilehash: 7653d7a56302deaad75443746ff7e83834af260f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571357"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="4a27e-103">Propriedade canônica PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="4a27e-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="4a27e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a27e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a27e-105">Indica que a exceção mensagem incorporada do objeto tem um corpo que difere do objeto de calendário recorrente.</span><span class="sxs-lookup"><span data-stu-id="4a27e-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a27e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4a27e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a27e-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="4a27e-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="4a27e-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="4a27e-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a27e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4a27e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4a27e-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="4a27e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a27e-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="4a27e-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="4a27e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4a27e-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a27e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4a27e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4a27e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4a27e-114">Area:</span></span>  <br/> |<span data-ttu-id="4a27e-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="4a27e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a27e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a27e-116">Remarks</span></span>

<span data-ttu-id="4a27e-117">Se o valor dessa propriedade for TRUE, a exceção incorporada objeto deve ter um corpo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a27e-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="4a27e-118">Se o valor dessa propriedade é FALSE, ou se a propriedade não existir, um cliente ou servidor deve obter o corpo do objeto de calendário recorrente.</span><span class="sxs-lookup"><span data-stu-id="4a27e-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a27e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a27e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a27e-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4a27e-120">Protocol specifications</span></span>

<span data-ttu-id="4a27e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a27e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a27e-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4a27e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a27e-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a27e-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a27e-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="4a27e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a27e-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a27e-125">Header files</span></span>

<span data-ttu-id="4a27e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a27e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a27e-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4a27e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a27e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a27e-128">See also</span></span>



[<span data-ttu-id="4a27e-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a27e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a27e-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4a27e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a27e-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4a27e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a27e-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4a27e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

