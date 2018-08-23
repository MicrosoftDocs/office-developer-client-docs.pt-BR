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
ms.openlocfilehash: 60704464beb162a614d6619b5e74d362b4af4488
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585105"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="e85a5-103">Propriedade canônica PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="e85a5-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="e85a5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e85a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e85a5-105">Contém um número positivo cujo negativo é menor ou igual ao valor da propriedade **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de todas as tarefas na pasta.</span><span class="sxs-lookup"><span data-stu-id="e85a5-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e85a5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e85a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e85a5-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="e85a5-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="e85a5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e85a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e85a5-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="e85a5-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="e85a5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e85a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="e85a5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e85a5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e85a5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e85a5-112">Area:</span></span>  <br/> |<span data-ttu-id="e85a5-113">Task</span><span class="sxs-lookup"><span data-stu-id="e85a5-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e85a5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e85a5-114">Remarks</span></span>

<span data-ttu-id="e85a5-115">Esta propriedade deve ser atualizada para manter essa condição sempre que a propriedade **dispidTaskOrdinal** de qualquer objeto de tarefa na pasta é alterada de forma que violaria a condição.</span><span class="sxs-lookup"><span data-stu-id="e85a5-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e85a5-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e85a5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e85a5-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e85a5-117">Protocol specifications</span></span>

<span data-ttu-id="e85a5-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85a5-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85a5-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e85a5-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e85a5-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e85a5-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e85a5-121">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="e85a5-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="e85a5-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e85a5-122">Header files</span></span>

<span data-ttu-id="e85a5-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e85a5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e85a5-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e85a5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e85a5-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e85a5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e85a5-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e85a5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e85a5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e85a5-127">See also</span></span>



[<span data-ttu-id="e85a5-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e85a5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e85a5-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e85a5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e85a5-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e85a5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e85a5-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e85a5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

