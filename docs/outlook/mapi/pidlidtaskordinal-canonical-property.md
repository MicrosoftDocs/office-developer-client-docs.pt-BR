---
title: Propriedade canônica PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357957"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="a6a7d-103">Propriedade canônica PidLidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="a6a7d-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="a6a7d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6a7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6a7d-105">Fornece um auxílio para tarefas de classificação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6a7d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a6a7d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6a7d-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="a6a7d-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="a6a7d-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="a6a7d-108">Property set:</span></span>  <br/> |<span data-ttu-id="a6a7d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a6a7d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a6a7d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a6a7d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a6a7d-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="a6a7d-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="a6a7d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a6a7d-112">Data type:</span></span>  <br/> |<span data-ttu-id="a6a7d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a6a7d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a6a7d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a6a7d-114">Area:</span></span>  <br/> |<span data-ttu-id="a6a7d-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="a6a7d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6a7d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6a7d-116">Remarks</span></span>

<span data-ttu-id="a6a7d-117">Essa propriedade pode ser deixada desalinhada.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-117">This property may be left unset.</span></span> <span data-ttu-id="a6a7d-118">Se definido, seu valor deve ser maior que "0x800186A0" (-2.147.383.648) e menor que "0x7FFE7960" (2.147.383.648) e deve ser exclusivo entre tarefas na mesma pasta.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="a6a7d-119">Sempre que o cliente define essa propriedade como um número menor que o negativo do valor atual da propriedade **PR_ORDINAL_MOST** (  [PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) da pasta, o cliente também deve atualizar PR_ORDINAL_MOST na pasta.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="a6a7d-120">A **PR_ORDINAL_MOST** propriedade da pasta fornece uma maneira eficiente de determinar um valor exclusivo entre tarefas na mesma pasta.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a6a7d-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6a7d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6a7d-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a6a7d-122">Protocol specifications</span></span>

<span data-ttu-id="a6a7d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6a7d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6a7d-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a6a7d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6a7d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6a7d-126">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="a6a7d-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a6a7d-127">Header files</span></span>

<span data-ttu-id="a6a7d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6a7d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6a7d-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a6a7d-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6a7d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6a7d-130">See also</span></span>



[<span data-ttu-id="a6a7d-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a6a7d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6a7d-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a6a7d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6a7d-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a6a7d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6a7d-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a6a7d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

