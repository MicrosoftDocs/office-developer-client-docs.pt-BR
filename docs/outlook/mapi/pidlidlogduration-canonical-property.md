---
title: Propriedade canônica PidLidLogDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336915"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="299ba-103">Propriedade canônica PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="299ba-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="299ba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="299ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="299ba-105">Representa a duração, em minutos, de uma mensagem de diário.</span><span class="sxs-lookup"><span data-stu-id="299ba-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="299ba-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="299ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="299ba-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="299ba-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="299ba-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="299ba-108">Property set:</span></span>  <br/> |<span data-ttu-id="299ba-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="299ba-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="299ba-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="299ba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="299ba-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="299ba-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="299ba-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="299ba-112">Data type:</span></span>  <br/> |<span data-ttu-id="299ba-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="299ba-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="299ba-114">Área:</span><span class="sxs-lookup"><span data-stu-id="299ba-114">Area:</span></span>  <br/> |<span data-ttu-id="299ba-115">Diário</span><span class="sxs-lookup"><span data-stu-id="299ba-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="299ba-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="299ba-116">Remarks</span></span>

<span data-ttu-id="299ba-117">A duração, em minutos, da atividade que deve ser a diferença entre as propriedades **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) e **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="299ba-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="299ba-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="299ba-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="299ba-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="299ba-119">Protocol specifications</span></span>

<span data-ttu-id="299ba-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="299ba-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="299ba-121">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="299ba-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="299ba-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="299ba-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="299ba-123">Especifica as propriedades e as operações que são permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="299ba-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="299ba-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="299ba-124">Header files</span></span>

<span data-ttu-id="299ba-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="299ba-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="299ba-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="299ba-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="299ba-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="299ba-127">See also</span></span>



[<span data-ttu-id="299ba-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="299ba-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="299ba-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="299ba-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="299ba-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="299ba-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="299ba-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="299ba-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

