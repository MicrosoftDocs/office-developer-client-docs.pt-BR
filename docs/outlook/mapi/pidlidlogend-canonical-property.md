---
title: Propriedade canônica PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ef1c9814aa6d1f81a44883d09ac635a5eed76517
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768527"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="cc19f-103">Propriedade canônica PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="cc19f-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="cc19f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc19f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc19f-105">Representa a data de término e a hora da mensagem de diário.</span><span class="sxs-lookup"><span data-stu-id="cc19f-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc19f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cc19f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc19f-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="cc19f-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="cc19f-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="cc19f-108">Property set:</span></span>  <br/> |<span data-ttu-id="cc19f-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="cc19f-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="cc19f-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="cc19f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cc19f-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="cc19f-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="cc19f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cc19f-112">Data type:</span></span>  <br/> |<span data-ttu-id="cc19f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="cc19f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="cc19f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="cc19f-114">Area:</span></span>  <br/> |<span data-ttu-id="cc19f-115">Diário</span><span class="sxs-lookup"><span data-stu-id="cc19f-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc19f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc19f-116">Remarks</span></span>

<span data-ttu-id="cc19f-117">A hora em que a atividade terminou no tempo Universal Coordenado The (UTC), que deve ser igual à propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) e maior ou igual à propriedade **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc19f-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc19f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc19f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc19f-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cc19f-119">Protocol specifications</span></span>

<span data-ttu-id="cc19f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc19f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc19f-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="cc19f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc19f-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc19f-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc19f-123">Especifica as propriedades e operações que são permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="cc19f-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc19f-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cc19f-124">Header files</span></span>

<span data-ttu-id="cc19f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc19f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc19f-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cc19f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc19f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc19f-127">See also</span></span>



[<span data-ttu-id="cc19f-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc19f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc19f-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cc19f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc19f-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cc19f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc19f-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cc19f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

