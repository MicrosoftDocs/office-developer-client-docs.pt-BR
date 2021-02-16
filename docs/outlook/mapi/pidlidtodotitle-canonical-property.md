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
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339939"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="11f12-103">Propriedade canônica PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="11f12-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="11f12-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11f12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11f12-105">Contém texto especificado pelo usuário para identificar esse objeto de mensagem em uma lista de a fazer consolidada.</span><span class="sxs-lookup"><span data-stu-id="11f12-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11f12-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="11f12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11f12-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="11f12-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="11f12-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="11f12-108">Property set:</span></span>  <br/> |<span data-ttu-id="11f12-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="11f12-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="11f12-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="11f12-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="11f12-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="11f12-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="11f12-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="11f12-112">Data type:</span></span>  <br/> |<span data-ttu-id="11f12-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11f12-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="11f12-114">Área:</span><span class="sxs-lookup"><span data-stu-id="11f12-114">Area:</span></span>  <br/> |<span data-ttu-id="11f12-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="11f12-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11f12-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="11f12-116">Remarks</span></span>

<span data-ttu-id="11f12-117">Essa propriedade não deve ser definida em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="11f12-117">This property must not be set on a task.</span></span> <span data-ttu-id="11f12-118">Para indicar uma propriedade vazia, não de definida como a cadeia de caracteres de comprimento zero; em vez disso, exclua-a.</span><span class="sxs-lookup"><span data-stu-id="11f12-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="11f12-119">Ao sinalizar um objeto de mensagem e a propriedade não existir, um cliente deve gravar o valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="11f12-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="11f12-120">Em uma lista de coisas a fazer consolidada, se essa propriedade não existir, um cliente deverá substituir o valor da propriedade **PR_NORMALIZED_SUBJECT** ao exibir essa propriedade na lista de a fazer.</span><span class="sxs-lookup"><span data-stu-id="11f12-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="11f12-121">Em um objeto de mensagem de rascunho, se o cliente implementa sinalizadores de remetente, essa propriedade deve ser definida com o mesmo valor que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="11f12-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11f12-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="11f12-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11f12-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="11f12-123">Protocol specifications</span></span>

<span data-ttu-id="11f12-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11f12-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11f12-125">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server</span><span class="sxs-lookup"><span data-stu-id="11f12-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="11f12-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11f12-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11f12-127">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="11f12-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11f12-128">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="11f12-128">Header files</span></span>

<span data-ttu-id="11f12-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11f12-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="11f12-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="11f12-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11f12-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="11f12-131">See also</span></span>



[<span data-ttu-id="11f12-132">Propriedade canônica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="11f12-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="11f12-133">Propriedade can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="11f12-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="11f12-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="11f12-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11f12-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="11f12-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11f12-136">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="11f12-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11f12-137">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="11f12-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

