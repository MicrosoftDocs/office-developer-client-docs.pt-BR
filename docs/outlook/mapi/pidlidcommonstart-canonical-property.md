---
title: Propriedade canônica PidLidCommonStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d0d72f3ca63930f1a8df7818e4ce4a34e8d11e71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567773"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="9521a-103">Propriedade canônica PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="9521a-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="9521a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9521a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9521a-105">Representa a data de início e a hora de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9521a-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9521a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9521a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9521a-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="9521a-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="9521a-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="9521a-108">Property set:</span></span>  <br/> |<span data-ttu-id="9521a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9521a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9521a-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="9521a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9521a-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="9521a-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="9521a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9521a-112">Data type:</span></span>  <br/> |<span data-ttu-id="9521a-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9521a-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9521a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9521a-114">Area:</span></span>  <br/> |<span data-ttu-id="9521a-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="9521a-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9521a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9521a-116">Remarks</span></span>

<span data-ttu-id="9521a-117">Esta propriedade indica a hora de início para um item.</span><span class="sxs-lookup"><span data-stu-id="9521a-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="9521a-118">Ela deve ser menor ou igual ao valor da propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9521a-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="9521a-119">O valor dessa propriedade deve ser o equivalente de tempo Universal Coordenado (UTC) da propriedade **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9521a-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9521a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9521a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9521a-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9521a-121">Protocol specifications</span></span>

<span data-ttu-id="9521a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9521a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9521a-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9521a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9521a-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9521a-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9521a-125">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="9521a-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9521a-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9521a-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9521a-127">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="9521a-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9521a-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9521a-128">Header files</span></span>

<span data-ttu-id="9521a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9521a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9521a-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9521a-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9521a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9521a-131">See also</span></span>



[<span data-ttu-id="9521a-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9521a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9521a-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9521a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9521a-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9521a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9521a-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9521a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

