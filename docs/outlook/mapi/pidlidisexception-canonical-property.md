---
title: Propriedade canônica PidLidIsException
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5a36cf21a36f83ec252923ddbb137b3b99456927
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768503"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="abd5e-103">Propriedade canônica PidLidIsException</span><span class="sxs-lookup"><span data-stu-id="abd5e-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="abd5e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="abd5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="abd5e-105">Indica que o objeto que representa uma exceção (incluindo uma instância órfão).</span><span class="sxs-lookup"><span data-stu-id="abd5e-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abd5e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="abd5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abd5e-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="abd5e-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="abd5e-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="abd5e-108">Property set:</span></span>  <br/> |<span data-ttu-id="abd5e-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="abd5e-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="abd5e-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="abd5e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="abd5e-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="abd5e-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="abd5e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="abd5e-112">Data type:</span></span>  <br/> |<span data-ttu-id="abd5e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="abd5e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="abd5e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="abd5e-114">Area:</span></span>  <br/> |<span data-ttu-id="abd5e-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="abd5e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abd5e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="abd5e-116">Remarks</span></span>

<span data-ttu-id="abd5e-117">Um valor FALSE indica que o objeto que representa uma única instância ou uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="abd5e-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="abd5e-118">A ausência dessa propriedade para qualquer objeto indica um valor falso, exceto a mensagem de exceção de incorporado, que assume um valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="abd5e-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abd5e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="abd5e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abd5e-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="abd5e-120">Protocol specifications</span></span>

<span data-ttu-id="abd5e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abd5e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abd5e-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="abd5e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abd5e-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abd5e-123">[[MS-OXOCAL] ](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abd5e-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="abd5e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abd5e-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="abd5e-125">Header files</span></span>

<span data-ttu-id="abd5e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abd5e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="abd5e-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="abd5e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abd5e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="abd5e-128">See also</span></span>



[<span data-ttu-id="abd5e-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="abd5e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abd5e-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="abd5e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abd5e-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="abd5e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abd5e-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="abd5e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

