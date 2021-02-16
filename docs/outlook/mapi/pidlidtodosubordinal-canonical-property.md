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
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344916"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="467ce-103">Propriedade canônica PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="467ce-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="467ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="467ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="467ce-105">Atua como um desempate quando a **propriedade dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) classifica objetos e o resultado em um vínculo.</span><span class="sxs-lookup"><span data-stu-id="467ce-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="467ce-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="467ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="467ce-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="467ce-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="467ce-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="467ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="467ce-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="467ce-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="467ce-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="467ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="467ce-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="467ce-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="467ce-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="467ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="467ce-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="467ce-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="467ce-114">Área:</span><span class="sxs-lookup"><span data-stu-id="467ce-114">Area:</span></span>  <br/> |<span data-ttu-id="467ce-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="467ce-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="467ce-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="467ce-116">Remarks</span></span>

<span data-ttu-id="467ce-117">Se usada, essa propriedade deve ser ordenada lexicograficamente.</span><span class="sxs-lookup"><span data-stu-id="467ce-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="467ce-118">Os caracteres componentes da cadeia de caracteres devem consistir apenas nos numerais zero a nove.</span><span class="sxs-lookup"><span data-stu-id="467ce-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="467ce-119">Essa propriedade deve ser inicialmente definida como "5555555".</span><span class="sxs-lookup"><span data-stu-id="467ce-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="467ce-120">O comprimento dessa propriedade não deve exceder 254 caracteres (excluindo o caractere NULL de encerramento).</span><span class="sxs-lookup"><span data-stu-id="467ce-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="467ce-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="467ce-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="467ce-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="467ce-122">Protocol specifications</span></span>

<span data-ttu-id="467ce-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="467ce-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="467ce-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="467ce-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="467ce-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="467ce-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="467ce-126">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="467ce-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="467ce-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="467ce-127">Header files</span></span>

<span data-ttu-id="467ce-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="467ce-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="467ce-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="467ce-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="467ce-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="467ce-130">See also</span></span>



[<span data-ttu-id="467ce-131">Propriedade canônica PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="467ce-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="467ce-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="467ce-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="467ce-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="467ce-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="467ce-134">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="467ce-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="467ce-135">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="467ce-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

