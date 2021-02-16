---
title: Propriedade canônica PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303035"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="1f5eb-103">Propriedade canônica PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="1f5eb-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="1f5eb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f5eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f5eb-105">Indica a precisão da **propriedade dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f5eb-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f5eb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1f5eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f5eb-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="1f5eb-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="1f5eb-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="1f5eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="1f5eb-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1f5eb-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1f5eb-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1f5eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1f5eb-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="1f5eb-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="1f5eb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f5eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="1f5eb-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1f5eb-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1f5eb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1f5eb-114">Area:</span></span>  <br/> |<span data-ttu-id="1f5eb-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="1f5eb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f5eb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f5eb-116">Remarks</span></span>

<span data-ttu-id="1f5eb-117">Se a **propriedade dispidTaskFFixOffline** estiver definida como FALSE ou não definida, o valor da propriedade **dispidTaskOwner** será correto.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="1f5eb-118">Se **dispidTaskFFixOffline** for definido como TRUE, o cliente não poderá determinar um valor preciso para **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="1f5eb-119">Nesse caso, o cliente pode definir **dispidTaskOwner** como um nome de proprietário genérico, como "Desconhecido".</span><span class="sxs-lookup"><span data-stu-id="1f5eb-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="1f5eb-120">No entanto, se um cliente encontrar um valor **dispidTaskFFixOffline** de TRUE e puder determinar um nome de proprietário preciso, o cliente deverá atualizar **dispidTaskOwner** e definir **dispidTaskFFixOffline** como FALSE.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f5eb-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f5eb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f5eb-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1f5eb-122">Protocol specifications</span></span>

<span data-ttu-id="1f5eb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f5eb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f5eb-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f5eb-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f5eb-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f5eb-126">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="1f5eb-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1f5eb-127">Header files</span></span>

<span data-ttu-id="1f5eb-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f5eb-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f5eb-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f5eb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f5eb-130">See also</span></span>



[<span data-ttu-id="1f5eb-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1f5eb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f5eb-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1f5eb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f5eb-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1f5eb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f5eb-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1f5eb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

