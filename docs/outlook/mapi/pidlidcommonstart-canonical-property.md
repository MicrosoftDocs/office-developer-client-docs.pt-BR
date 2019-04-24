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
ms.openlocfilehash: ec7c213d7eec9ab0ef5766442e3de59a24811d37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345483"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="eb93b-103">Propriedade canônica PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="eb93b-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="eb93b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb93b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb93b-105">Representa a data de início e a hora de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb93b-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb93b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="eb93b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb93b-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="eb93b-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="eb93b-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="eb93b-108">Property set:</span></span>  <br/> |<span data-ttu-id="eb93b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="eb93b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="eb93b-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="eb93b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eb93b-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="eb93b-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="eb93b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="eb93b-112">Data type:</span></span>  <br/> |<span data-ttu-id="eb93b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="eb93b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="eb93b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="eb93b-114">Area:</span></span>  <br/> |<span data-ttu-id="eb93b-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="eb93b-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb93b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb93b-116">Remarks</span></span>

<span data-ttu-id="eb93b-117">Esta propriedade indica a hora de início de um item.</span><span class="sxs-lookup"><span data-stu-id="eb93b-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="eb93b-118">Ele deve ser menor ou igual ao valor da propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eb93b-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="eb93b-119">O valor dessa propriedade deve ser o equivalente de tempo universal coordenado (UTC) da propriedade **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eb93b-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb93b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb93b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb93b-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="eb93b-121">Protocol specifications</span></span>

<span data-ttu-id="eb93b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb93b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb93b-123">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="eb93b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb93b-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb93b-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb93b-125">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="eb93b-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="eb93b-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb93b-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb93b-127">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="eb93b-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb93b-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eb93b-128">Header files</span></span>

<span data-ttu-id="eb93b-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="eb93b-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb93b-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="eb93b-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb93b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb93b-131">See also</span></span>



[<span data-ttu-id="eb93b-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="eb93b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb93b-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="eb93b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb93b-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="eb93b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb93b-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="eb93b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

