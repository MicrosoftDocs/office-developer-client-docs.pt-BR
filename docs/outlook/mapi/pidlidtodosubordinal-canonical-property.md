---
title: Propriedade canônica PidLidToDoSubOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9965ed059ba4596232111f5fbd86b9d177e3c3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768743"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="708dd-103">Propriedade canônica PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="708dd-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="708dd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="708dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="708dd-105">Atua como um separador de tie quando a propriedade **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) classifica os objetos e o resultado em uma ligação.</span><span class="sxs-lookup"><span data-stu-id="708dd-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="708dd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="708dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="708dd-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="708dd-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="708dd-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="708dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="708dd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="708dd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="708dd-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="708dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="708dd-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="708dd-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="708dd-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="708dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="708dd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="708dd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="708dd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="708dd-114">Area:</span></span>  <br/> |<span data-ttu-id="708dd-115">Task</span><span class="sxs-lookup"><span data-stu-id="708dd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="708dd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="708dd-116">Remarks</span></span>

<span data-ttu-id="708dd-117">Se usado, esta propriedade deve ser classificada lexicograficamente.</span><span class="sxs-lookup"><span data-stu-id="708dd-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="708dd-118">Os caracteres de componente da cadeia de caracteres devem conter apenas os numerais zero a nove.</span><span class="sxs-lookup"><span data-stu-id="708dd-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="708dd-119">Esta propriedade deve ser definida inicialmente como "5555555".</span><span class="sxs-lookup"><span data-stu-id="708dd-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="708dd-120">O comprimento dessa propriedade não deve exceder 254 caracteres (excluindo o caractere de terminação NULL).</span><span class="sxs-lookup"><span data-stu-id="708dd-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="708dd-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="708dd-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="708dd-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="708dd-122">Protocol specifications</span></span>

<span data-ttu-id="708dd-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="708dd-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="708dd-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="708dd-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="708dd-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="708dd-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="708dd-126">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="708dd-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="708dd-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="708dd-127">Header files</span></span>

<span data-ttu-id="708dd-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="708dd-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="708dd-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="708dd-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="708dd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="708dd-130">See also</span></span>



[<span data-ttu-id="708dd-131">Propriedade canônica PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="708dd-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="708dd-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="708dd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="708dd-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="708dd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="708dd-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="708dd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="708dd-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="708dd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

