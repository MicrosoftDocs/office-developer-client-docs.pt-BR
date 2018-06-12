---
title: Propriedade canônico de PidLidTaskAccepted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7448768a0a35cbf53b481eab0571b405fead1544
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768688"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="46f56-103">Propriedade canônico de PidLidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="46f56-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="46f56-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46f56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46f56-105">Indica se um destinatário de tarefa respondeu a uma solicitação de tarefa.</span><span class="sxs-lookup"><span data-stu-id="46f56-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46f56-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="46f56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46f56-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="46f56-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="46f56-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="46f56-108">Property set:</span></span>  <br/> |<span data-ttu-id="46f56-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="46f56-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="46f56-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="46f56-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="46f56-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="46f56-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="46f56-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="46f56-112">Data type:</span></span>  <br/> |<span data-ttu-id="46f56-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="46f56-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="46f56-114">Área:</span><span class="sxs-lookup"><span data-stu-id="46f56-114">Area:</span></span>  <br/> |<span data-ttu-id="46f56-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="46f56-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46f56-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="46f56-116">Remarks</span></span>

<span data-ttu-id="46f56-117">O cliente define essa propriedade como FALSE para uma nova tarefa ou o cliente define essa propriedade como TRUE quando uma tarefa é aceita ou rejeitada.</span><span class="sxs-lookup"><span data-stu-id="46f56-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="46f56-118">Se a propriedade for deixada não definida, um valor FALSE é assumido.</span><span class="sxs-lookup"><span data-stu-id="46f56-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46f56-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46f56-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46f56-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="46f56-120">Protocol specifications</span></span>

<span data-ttu-id="46f56-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f56-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f56-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="46f56-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46f56-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46f56-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46f56-124">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="46f56-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46f56-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46f56-125">Header files</span></span>

<span data-ttu-id="46f56-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46f56-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="46f56-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="46f56-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46f56-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="46f56-128">See also</span></span>



[<span data-ttu-id="46f56-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46f56-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46f56-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="46f56-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46f56-131">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="46f56-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46f56-132">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="46f56-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

