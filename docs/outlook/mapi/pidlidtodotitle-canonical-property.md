---
title: Propriedade canônica PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 66208b2d31ca379389f3249abf281dd4d040e276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768748"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="16dfe-103">Propriedade canônica PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="16dfe-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="16dfe-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16dfe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16dfe-105">Contém o texto especificáveis de usuário para identificar este objeto de mensagem em uma lista de tarefas pendentes consolidada.</span><span class="sxs-lookup"><span data-stu-id="16dfe-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16dfe-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="16dfe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16dfe-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="16dfe-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="16dfe-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="16dfe-108">Property set:</span></span>  <br/> |<span data-ttu-id="16dfe-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="16dfe-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="16dfe-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="16dfe-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="16dfe-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="16dfe-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="16dfe-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="16dfe-112">Data type:</span></span>  <br/> |<span data-ttu-id="16dfe-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16dfe-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="16dfe-114">Área:</span><span class="sxs-lookup"><span data-stu-id="16dfe-114">Area:</span></span>  <br/> |<span data-ttu-id="16dfe-115">Task</span><span class="sxs-lookup"><span data-stu-id="16dfe-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16dfe-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="16dfe-116">Remarks</span></span>

<span data-ttu-id="16dfe-117">Essa propriedade não deve ser definida em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="16dfe-117">This property must not be set on a task.</span></span> <span data-ttu-id="16dfe-118">Para indicar uma propriedade vazia, não definir essa propriedade para a cadeia de caracteres de comprimento zero, mas, em vez disso, excluí-la.</span><span class="sxs-lookup"><span data-stu-id="16dfe-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="16dfe-119">Quando um objeto de mensagem e a propriedade de sinalização não existe, um cliente deve gravar o valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="16dfe-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="16dfe-120">Em uma lista de tarefas pendentes consolidada, se essa propriedade não existir, um cliente deve substituir o valor da propriedade **PR_NORMALIZED_SUBJECT** ao exibir essa propriedade na lista de tarefas pendentes.</span><span class="sxs-lookup"><span data-stu-id="16dfe-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="16dfe-121">Em um objeto de mensagem de rascunho, se o cliente implementa sinalizadores de remetente, essa propriedade deve ser definida com o mesmo valor **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="16dfe-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="16dfe-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="16dfe-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16dfe-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="16dfe-123">Protocol specifications</span></span>

<span data-ttu-id="16dfe-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16dfe-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16dfe-125">Fornece as definições do conjunto de propriedades e referências para relacionados especificações de protocolo do Exchange Server</span><span class="sxs-lookup"><span data-stu-id="16dfe-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="16dfe-126">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16dfe-126">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16dfe-127">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="16dfe-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="16dfe-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="16dfe-128">Header files</span></span>

<span data-ttu-id="16dfe-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16dfe-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="16dfe-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="16dfe-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16dfe-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="16dfe-131">See also</span></span>



[<span data-ttu-id="16dfe-132">Propriedade canônica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="16dfe-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="16dfe-133">Propriedade can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="16dfe-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="16dfe-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="16dfe-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16dfe-135">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="16dfe-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16dfe-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="16dfe-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16dfe-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="16dfe-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

