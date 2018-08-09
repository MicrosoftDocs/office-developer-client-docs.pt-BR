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
ms.openlocfilehash: e2d3dee4d268a1747d6b77acf62f24c6ec459bdc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768338"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="f22dd-103">Propriedade canônica PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="f22dd-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="f22dd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f22dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f22dd-105">Representa a data de início e a hora de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f22dd-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f22dd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f22dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f22dd-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="f22dd-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="f22dd-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="f22dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="f22dd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f22dd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f22dd-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="f22dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f22dd-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="f22dd-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="f22dd-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f22dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="f22dd-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f22dd-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f22dd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f22dd-114">Area:</span></span>  <br/> |<span data-ttu-id="f22dd-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="f22dd-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f22dd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f22dd-116">Remarks</span></span>

<span data-ttu-id="f22dd-117">Esta propriedade indica a hora de início para um item.</span><span class="sxs-lookup"><span data-stu-id="f22dd-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="f22dd-118">Ela deve ser menor ou igual ao valor da propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f22dd-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f22dd-119">O valor dessa propriedade deve ser o equivalente de tempo Universal Coordenado (UTC) da propriedade **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f22dd-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f22dd-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f22dd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f22dd-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f22dd-121">Protocol specifications</span></span>

<span data-ttu-id="f22dd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f22dd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f22dd-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f22dd-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f22dd-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f22dd-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f22dd-125">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="f22dd-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f22dd-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f22dd-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f22dd-127">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="f22dd-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f22dd-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f22dd-128">Header files</span></span>

<span data-ttu-id="f22dd-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f22dd-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f22dd-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f22dd-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f22dd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f22dd-131">See also</span></span>



[<span data-ttu-id="f22dd-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f22dd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f22dd-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f22dd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f22dd-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f22dd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f22dd-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f22dd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

