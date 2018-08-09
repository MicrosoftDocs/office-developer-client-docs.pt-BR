---
title: Propriedade canônica PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0782191010341019ebea71ebf545dec490521520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768671"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="327e6-103">Propriedade canônica PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="327e6-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="327e6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="327e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="327e6-105">Indica o número de minutos que o usuário realizou uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="327e6-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="327e6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="327e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="327e6-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="327e6-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="327e6-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="327e6-108">Property set:</span></span>  <br/> |<span data-ttu-id="327e6-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="327e6-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="327e6-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="327e6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="327e6-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="327e6-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="327e6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="327e6-112">Data type:</span></span>  <br/> |<span data-ttu-id="327e6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="327e6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="327e6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="327e6-114">Area:</span></span>  <br/> |<span data-ttu-id="327e6-115">Task</span><span class="sxs-lookup"><span data-stu-id="327e6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="327e6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="327e6-116">Remarks</span></span>

<span data-ttu-id="327e6-117">O valor deve ser maior ou igual a 0 e menor que 0x5AE980DF (1,525,252,319), onde o 480 minutos igual a um dia e 2400 minutos igual uma semana (oito horas em um dia de trabalho e cinco dias em uma semana de trabalho).</span><span class="sxs-lookup"><span data-stu-id="327e6-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="327e6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="327e6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="327e6-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="327e6-119">Protocol specifications</span></span>

<span data-ttu-id="327e6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="327e6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="327e6-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="327e6-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="327e6-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="327e6-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="327e6-123">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="327e6-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="327e6-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="327e6-124">Header files</span></span>

<span data-ttu-id="327e6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="327e6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="327e6-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="327e6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="327e6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="327e6-127">See also</span></span>



[<span data-ttu-id="327e6-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="327e6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="327e6-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="327e6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="327e6-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="327e6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="327e6-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="327e6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

