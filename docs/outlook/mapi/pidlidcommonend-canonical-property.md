---
title: Propriedade canônica PidLidCommonEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 97d6ef6343cedb6fbed93cccda9f65476bb73f4f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393303"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="78769-103">Propriedade canônica PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="78769-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="78769-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78769-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78769-105">Representa a data de término e a hora de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="78769-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78769-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="78769-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78769-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="78769-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="78769-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="78769-108">Property set:</span></span>  <br/> |<span data-ttu-id="78769-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="78769-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="78769-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="78769-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="78769-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="78769-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="78769-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="78769-112">Data type:</span></span>  <br/> |<span data-ttu-id="78769-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="78769-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="78769-114">Área:</span><span class="sxs-lookup"><span data-stu-id="78769-114">Area:</span></span>  <br/> |<span data-ttu-id="78769-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="78769-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78769-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="78769-116">Remarks</span></span>

<span data-ttu-id="78769-117">Esta propriedade indica a hora de término para um item.</span><span class="sxs-lookup"><span data-stu-id="78769-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="78769-118">Ele deve ser maior ou igual ao valor da propriedade **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="78769-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="78769-119">Este valor deve ser o equivalente de tempo Universal Coordenado (UTC) da propriedade **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="78769-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78769-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="78769-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78769-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="78769-121">Protocol specifications</span></span>

<span data-ttu-id="78769-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78769-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78769-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="78769-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78769-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78769-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78769-125">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="78769-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="78769-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78769-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78769-127">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="78769-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78769-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="78769-128">Header files</span></span>

<span data-ttu-id="78769-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78769-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="78769-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="78769-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78769-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="78769-131">See also</span></span>



[<span data-ttu-id="78769-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="78769-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78769-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="78769-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78769-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="78769-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78769-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="78769-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

