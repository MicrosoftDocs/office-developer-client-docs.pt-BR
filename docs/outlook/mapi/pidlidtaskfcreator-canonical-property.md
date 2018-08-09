---
title: Propriedade canônica PidLidTaskFCreator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 458a20e238d6023520ede3416ece239f2d553891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768703"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="11cf4-103">Propriedade canônica PidLidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="11cf4-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="11cf4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11cf4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11cf4-105">Indica que a tarefa foi originalmente criada pelo usuário atual ou agente do usuário, em vez de processar uma solicitação de tarefa.</span><span class="sxs-lookup"><span data-stu-id="11cf4-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11cf4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="11cf4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11cf4-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="11cf4-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="11cf4-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="11cf4-108">Property set:</span></span>  <br/> |<span data-ttu-id="11cf4-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="11cf4-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="11cf4-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="11cf4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="11cf4-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="11cf4-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="11cf4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="11cf4-112">Data type:</span></span>  <br/> |<span data-ttu-id="11cf4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="11cf4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="11cf4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="11cf4-114">Area:</span></span>  <br/> |<span data-ttu-id="11cf4-115">Task</span><span class="sxs-lookup"><span data-stu-id="11cf4-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11cf4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="11cf4-116">Remarks</span></span>

<span data-ttu-id="11cf4-117">O cliente faz essa propriedade como TRUE quando o usuário cria a tarefa e FALSE quando a tarefa é atribuída por outro usuário.</span><span class="sxs-lookup"><span data-stu-id="11cf4-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="11cf4-118">Se essa propriedade for deixada não definida, um valor TRUE é assumido.</span><span class="sxs-lookup"><span data-stu-id="11cf4-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11cf4-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="11cf4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11cf4-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="11cf4-120">Protocol specifications</span></span>

<span data-ttu-id="11cf4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11cf4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11cf4-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="11cf4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11cf4-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11cf4-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11cf4-124">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="11cf4-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11cf4-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="11cf4-125">Header files</span></span>

<span data-ttu-id="11cf4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11cf4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="11cf4-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="11cf4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11cf4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="11cf4-128">See also</span></span>



[<span data-ttu-id="11cf4-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="11cf4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11cf4-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="11cf4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11cf4-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="11cf4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11cf4-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="11cf4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

