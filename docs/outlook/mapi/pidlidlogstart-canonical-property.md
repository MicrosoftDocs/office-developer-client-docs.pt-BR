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
ms.openlocfilehash: 359eb4ea4cbbcf6244bf3cca2f3a66b369bce6e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586673"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="2c0b6-103">Propriedade canônica PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="2c0b6-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="2c0b6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c0b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c0b6-105">Representa a data de início e a hora da mensagem de diário.</span><span class="sxs-lookup"><span data-stu-id="2c0b6-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c0b6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2c0b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c0b6-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="2c0b6-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="2c0b6-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="2c0b6-108">Property set:</span></span>  <br/> |<span data-ttu-id="2c0b6-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="2c0b6-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="2c0b6-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="2c0b6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2c0b6-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="2c0b6-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="2c0b6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2c0b6-112">Data type:</span></span>  <br/> |<span data-ttu-id="2c0b6-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2c0b6-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2c0b6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2c0b6-114">Area:</span></span>  <br/> |<span data-ttu-id="2c0b6-115">Diário</span><span class="sxs-lookup"><span data-stu-id="2c0b6-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c0b6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c0b6-116">Remarks</span></span>

<span data-ttu-id="2c0b6-117">A hora no tempo Universal Coordenado (UTC) quando começou a atividade deve ser igual à propriedade **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c0b6-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c0b6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c0b6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c0b6-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c0b6-119">Protocol specifications</span></span>

<span data-ttu-id="2c0b6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c0b6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c0b6-121">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2c0b6-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c0b6-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c0b6-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c0b6-123">Especifica as propriedades e operações que são permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="2c0b6-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c0b6-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c0b6-124">Header files</span></span>

<span data-ttu-id="2c0b6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c0b6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c0b6-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2c0b6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c0b6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c0b6-127">See also</span></span>



[<span data-ttu-id="2c0b6-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c0b6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c0b6-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2c0b6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c0b6-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2c0b6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c0b6-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2c0b6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

