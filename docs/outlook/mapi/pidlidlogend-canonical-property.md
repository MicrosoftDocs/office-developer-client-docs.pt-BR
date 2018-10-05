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
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398938"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="8e9b9-103">Propriedade canônica PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="8e9b9-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="8e9b9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e9b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e9b9-105">Representa a data de término e a hora da mensagem de diário.</span><span class="sxs-lookup"><span data-stu-id="8e9b9-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e9b9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8e9b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e9b9-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="8e9b9-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="8e9b9-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="8e9b9-108">Property set:</span></span>  <br/> |<span data-ttu-id="8e9b9-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="8e9b9-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="8e9b9-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="8e9b9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8e9b9-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="8e9b9-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="8e9b9-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8e9b9-112">Data type:</span></span>  <br/> |<span data-ttu-id="8e9b9-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8e9b9-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8e9b9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8e9b9-114">Area:</span></span>  <br/> |<span data-ttu-id="8e9b9-115">Diário</span><span class="sxs-lookup"><span data-stu-id="8e9b9-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e9b9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e9b9-116">Remarks</span></span>

<span data-ttu-id="8e9b9-117">A hora em que a atividade terminou no tempo Universal Coordenado The (UTC), que deve ser igual à propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) e maior ou igual à propriedade **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e9b9-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e9b9-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e9b9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e9b9-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8e9b9-119">Protocol specifications</span></span>

<span data-ttu-id="8e9b9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e9b9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e9b9-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e9b9-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e9b9-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e9b9-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e9b9-123">Especifica as propriedades e operações que são permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="8e9b9-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e9b9-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e9b9-124">Header files</span></span>

<span data-ttu-id="8e9b9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e9b9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e9b9-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8e9b9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e9b9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e9b9-127">See also</span></span>



[<span data-ttu-id="8e9b9-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e9b9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e9b9-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8e9b9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e9b9-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e9b9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e9b9-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8e9b9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

