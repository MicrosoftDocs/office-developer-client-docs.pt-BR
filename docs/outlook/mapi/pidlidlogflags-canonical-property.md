---
title: Propriedade canônica PidLidLogFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f85fdc701a29f5865700c6519d589212a06fd0af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585777"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="1bb55-103">Propriedade canônica PidLidLogFlags</span><span class="sxs-lookup"><span data-stu-id="1bb55-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1bb55-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bb55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bb55-105">Inclui metadados sobre o diário.</span><span class="sxs-lookup"><span data-stu-id="1bb55-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1bb55-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1bb55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1bb55-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="1bb55-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="1bb55-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="1bb55-108">Property set:</span></span>  <br/> |<span data-ttu-id="1bb55-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="1bb55-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="1bb55-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="1bb55-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1bb55-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="1bb55-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="1bb55-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1bb55-112">Data type:</span></span>  <br/> |<span data-ttu-id="1bb55-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1bb55-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1bb55-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1bb55-114">Area:</span></span>  <br/> |<span data-ttu-id="1bb55-115">Diário</span><span class="sxs-lookup"><span data-stu-id="1bb55-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bb55-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bb55-116">Remarks</span></span>

<span data-ttu-id="1bb55-117">O campo de bit que contém metadados sobre o diário deve ser zero ou "0x40000000".</span><span class="sxs-lookup"><span data-stu-id="1bb55-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1bb55-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bb55-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1bb55-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1bb55-119">Protocol specifications</span></span>

<span data-ttu-id="1bb55-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bb55-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bb55-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1bb55-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1bb55-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bb55-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bb55-123">Especifica as propriedades e operações que são permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="1bb55-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1bb55-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1bb55-124">Header files</span></span>

<span data-ttu-id="1bb55-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1bb55-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1bb55-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bb55-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1bb55-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bb55-127">See also</span></span>



[<span data-ttu-id="1bb55-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1bb55-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1bb55-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1bb55-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1bb55-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1bb55-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1bb55-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1bb55-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

