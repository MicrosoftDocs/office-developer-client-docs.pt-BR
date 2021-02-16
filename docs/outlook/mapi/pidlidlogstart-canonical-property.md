---
title: Propriedade canônica PidLidLogStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dd5805cb0ee6b172506a532a513d06f57c583eee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337013"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="5f58d-103">Propriedade canônica PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="5f58d-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="5f58d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f58d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f58d-105">Representa a data e a hora de início da mensagem de diário.</span><span class="sxs-lookup"><span data-stu-id="5f58d-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f58d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5f58d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f58d-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="5f58d-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="5f58d-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="5f58d-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f58d-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="5f58d-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="5f58d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5f58d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5f58d-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="5f58d-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="5f58d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5f58d-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f58d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5f58d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5f58d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5f58d-114">Area:</span></span>  <br/> |<span data-ttu-id="5f58d-115">Diário</span><span class="sxs-lookup"><span data-stu-id="5f58d-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f58d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f58d-116">Remarks</span></span>

<span data-ttu-id="5f58d-117">O tempo em UTC (Tempo Universal Coordenado) em que a atividade começou deve ser igual à **propriedade dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f58d-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f58d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f58d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f58d-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5f58d-119">Protocol specifications</span></span>

<span data-ttu-id="5f58d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f58d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f58d-121">Fornece definição de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5f58d-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f58d-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f58d-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f58d-123">Especifica as propriedades e operações permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="5f58d-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f58d-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="5f58d-124">Header files</span></span>

<span data-ttu-id="5f58d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f58d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f58d-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5f58d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f58d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f58d-127">See also</span></span>



[<span data-ttu-id="5f58d-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f58d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f58d-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5f58d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f58d-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5f58d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f58d-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5f58d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

