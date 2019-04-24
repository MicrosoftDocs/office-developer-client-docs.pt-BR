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
ms.openlocfilehash: a407c065a51870ba9908fbd9b626d7f287a1df4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336943"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="3cd2e-103">Propriedade canônica PidLidLogFlags</span><span class="sxs-lookup"><span data-stu-id="3cd2e-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="3cd2e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cd2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cd2e-105">Contém metadados sobre o diário.</span><span class="sxs-lookup"><span data-stu-id="3cd2e-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cd2e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3cd2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cd2e-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="3cd2e-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="3cd2e-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="3cd2e-108">Property set:</span></span>  <br/> |<span data-ttu-id="3cd2e-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="3cd2e-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="3cd2e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3cd2e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3cd2e-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="3cd2e-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="3cd2e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3cd2e-112">Data type:</span></span>  <br/> |<span data-ttu-id="3cd2e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3cd2e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3cd2e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3cd2e-114">Area:</span></span>  <br/> |<span data-ttu-id="3cd2e-115">Diário</span><span class="sxs-lookup"><span data-stu-id="3cd2e-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cd2e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cd2e-116">Remarks</span></span>

<span data-ttu-id="3cd2e-117">O campo de bits que contém metadados sobre o diário deve ser zero ou "0x40000000".</span><span class="sxs-lookup"><span data-stu-id="3cd2e-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3cd2e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cd2e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cd2e-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="3cd2e-119">Protocol specifications</span></span>

<span data-ttu-id="3cd2e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cd2e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cd2e-121">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3cd2e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cd2e-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cd2e-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cd2e-123">Especifica as propriedades e as operações que são permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="3cd2e-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cd2e-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3cd2e-124">Header files</span></span>

<span data-ttu-id="3cd2e-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3cd2e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cd2e-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3cd2e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cd2e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cd2e-127">See also</span></span>



[<span data-ttu-id="3cd2e-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3cd2e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cd2e-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3cd2e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cd2e-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3cd2e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cd2e-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3cd2e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

