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
ms.openlocfilehash: a2adbee409649f0268d96502a7dd3f658433052a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768461"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="05372-103">Propriedade canônica PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="05372-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="05372-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05372-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05372-105">Indica que a exceção mensagem incorporada do objeto tem um corpo que difere do objeto de calendário recorrente.</span><span class="sxs-lookup"><span data-stu-id="05372-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05372-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="05372-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05372-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="05372-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="05372-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="05372-108">Property set:</span></span>  <br/> |<span data-ttu-id="05372-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="05372-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="05372-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="05372-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="05372-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="05372-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="05372-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="05372-112">Data type:</span></span>  <br/> |<span data-ttu-id="05372-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="05372-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="05372-114">Área:</span><span class="sxs-lookup"><span data-stu-id="05372-114">Area:</span></span>  <br/> |<span data-ttu-id="05372-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="05372-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05372-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="05372-116">Remarks</span></span>

<span data-ttu-id="05372-117">Se o valor dessa propriedade for TRUE, a exceção incorporada objeto deve ter um corpo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="05372-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="05372-118">Se o valor dessa propriedade é FALSE, ou se a propriedade não existir, um cliente ou servidor deve obter o corpo do objeto de calendário recorrente.</span><span class="sxs-lookup"><span data-stu-id="05372-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05372-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="05372-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05372-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="05372-120">Protocol specifications</span></span>

<span data-ttu-id="05372-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05372-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05372-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="05372-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05372-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05372-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05372-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="05372-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05372-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="05372-125">Header files</span></span>

<span data-ttu-id="05372-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05372-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="05372-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="05372-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05372-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="05372-128">See also</span></span>



[<span data-ttu-id="05372-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="05372-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05372-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="05372-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05372-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="05372-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05372-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="05372-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
