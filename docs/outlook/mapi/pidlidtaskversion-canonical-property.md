---
title: Propriedade canônica PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356487"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="4682b-103">Propriedade canônica PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="4682b-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="4682b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4682b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4682b-105">Indica qual cópia é a atualização mais recente de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="4682b-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4682b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4682b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4682b-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="4682b-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="4682b-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="4682b-108">Property set:</span></span>  <br/> |<span data-ttu-id="4682b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4682b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4682b-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4682b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4682b-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="4682b-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="4682b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4682b-112">Data type:</span></span>  <br/> |<span data-ttu-id="4682b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4682b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4682b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4682b-114">Area:</span></span>  <br/> |<span data-ttu-id="4682b-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="4682b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4682b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4682b-116">Remarks</span></span>

<span data-ttu-id="4682b-117">As atualizações com versões menores do que a tarefa são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="4682b-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="4682b-118">Ao incorporar uma tarefa em uma comunicação de tarefa, o cliente define a versão atual da tarefa incorporada também na comunicação da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4682b-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4682b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4682b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4682b-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="4682b-120">Protocol specifications</span></span>

<span data-ttu-id="4682b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4682b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4682b-122">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4682b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4682b-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4682b-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4682b-124">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4682b-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4682b-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4682b-125">Header files</span></span>

<span data-ttu-id="4682b-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4682b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4682b-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4682b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4682b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4682b-128">See also</span></span>



[<span data-ttu-id="4682b-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4682b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4682b-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4682b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4682b-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4682b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4682b-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4682b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

