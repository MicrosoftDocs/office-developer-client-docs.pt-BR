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
ms.openlocfilehash: 716d8b5b09ee0e29d1946042cae2631561d74df5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584650"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="57fa1-103">Propriedade canônica PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="57fa1-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="57fa1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57fa1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57fa1-105">Indica a precisão da propriedade **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="57fa1-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="57fa1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="57fa1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57fa1-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="57fa1-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="57fa1-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="57fa1-108">Property set:</span></span>  <br/> |<span data-ttu-id="57fa1-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="57fa1-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="57fa1-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="57fa1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="57fa1-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="57fa1-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="57fa1-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="57fa1-112">Data type:</span></span>  <br/> |<span data-ttu-id="57fa1-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="57fa1-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="57fa1-114">Área:</span><span class="sxs-lookup"><span data-stu-id="57fa1-114">Area:</span></span>  <br/> |<span data-ttu-id="57fa1-115">Task</span><span class="sxs-lookup"><span data-stu-id="57fa1-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57fa1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="57fa1-116">Remarks</span></span>

<span data-ttu-id="57fa1-117">Se a propriedade **dispidTaskFFixOffline** estiver definida como FALSE ou foi removida, o valor da propriedade **dispidTaskOwner** está correto.</span><span class="sxs-lookup"><span data-stu-id="57fa1-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="57fa1-118">Se **dispidTaskFFixOffline** for definido como TRUE, o cliente não pode determinar um valor exato para **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="57fa1-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="57fa1-119">Nesse caso, o cliente pode definir **dispidTaskOwner** para um nome de proprietário genérico, como "Desconhecido".</span><span class="sxs-lookup"><span data-stu-id="57fa1-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="57fa1-120">No entanto, se um cliente encontra um valor **dispidTaskFFixOffline** TRUE e pode determinar um nome de proprietário precisas, o cliente deve atualizar **dispidTaskOwner** e defina **dispidTaskFFixOffline** como FALSE.</span><span class="sxs-lookup"><span data-stu-id="57fa1-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="57fa1-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="57fa1-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="57fa1-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="57fa1-122">Protocol specifications</span></span>

<span data-ttu-id="57fa1-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57fa1-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57fa1-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="57fa1-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="57fa1-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57fa1-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57fa1-126">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="57fa1-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="57fa1-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="57fa1-127">Header files</span></span>

<span data-ttu-id="57fa1-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57fa1-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="57fa1-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="57fa1-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57fa1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="57fa1-130">See also</span></span>



[<span data-ttu-id="57fa1-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="57fa1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57fa1-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="57fa1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57fa1-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="57fa1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57fa1-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="57fa1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

