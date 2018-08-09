---
title: Propriedade canônica PidTagOrdinalMost
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0c2cf784ff9a86c9e2a2ce1a25b3c4b8ff7d8b75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769532"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="7681e-103">Propriedade canônica PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="7681e-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="7681e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7681e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7681e-105">Contém um número positivo cujo negativo é menor ou igual ao valor da propriedade **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de todas as tarefas na pasta.</span><span class="sxs-lookup"><span data-stu-id="7681e-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7681e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7681e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7681e-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="7681e-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="7681e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7681e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7681e-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="7681e-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="7681e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7681e-110">Data type:</span></span>  <br/> |<span data-ttu-id="7681e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7681e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7681e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7681e-112">Area:</span></span>  <br/> |<span data-ttu-id="7681e-113">Task</span><span class="sxs-lookup"><span data-stu-id="7681e-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7681e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7681e-114">Remarks</span></span>

<span data-ttu-id="7681e-115">Esta propriedade deve ser atualizada para manter essa condição sempre que a propriedade **dispidTaskOrdinal** de qualquer objeto de tarefa na pasta é alterada de forma que violaria a condição.</span><span class="sxs-lookup"><span data-stu-id="7681e-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7681e-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7681e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7681e-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7681e-117">Protocol specifications</span></span>

<span data-ttu-id="7681e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7681e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7681e-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7681e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7681e-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7681e-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7681e-121">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="7681e-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="7681e-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7681e-122">Header files</span></span>

<span data-ttu-id="7681e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7681e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7681e-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7681e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7681e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7681e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7681e-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7681e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7681e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7681e-127">See also</span></span>



[<span data-ttu-id="7681e-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7681e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7681e-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7681e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7681e-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7681e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7681e-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7681e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

