---
title: Propriedade canônica PidTagFlagCompleteTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316286"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="46fad-103">Propriedade canônica PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="46fad-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="46fad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46fad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46fad-105">Especifica a data e a hora no UTC (tempo Universal Coordenado) em que o objeto Message foi marcado como concluído.</span><span class="sxs-lookup"><span data-stu-id="46fad-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46fad-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="46fad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46fad-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="46fad-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="46fad-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="46fad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46fad-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="46fad-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="46fad-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="46fad-110">Data type:</span></span>  <br/> |<span data-ttu-id="46fad-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="46fad-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="46fad-112">Área:</span><span class="sxs-lookup"><span data-stu-id="46fad-112">Area:</span></span>  <br/> |<span data-ttu-id="46fad-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="46fad-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46fad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="46fad-114">Remarks</span></span>

<span data-ttu-id="46fad-115">Essa propriedade será excluída se o objeto Message não for marcado como concluído.</span><span class="sxs-lookup"><span data-stu-id="46fad-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="46fad-116">A menor resolução do tempo deve ser de minutos (o valor deve ser um múltiplo de 600 milhões).</span><span class="sxs-lookup"><span data-stu-id="46fad-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="46fad-117">Esta propriedade não deve existir se o objeto for um objeto relacionado à reunião e não existir em um objeto Task.</span><span class="sxs-lookup"><span data-stu-id="46fad-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46fad-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46fad-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46fad-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="46fad-119">Protocol specifications</span></span>

<span data-ttu-id="46fad-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46fad-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46fad-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="46fad-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46fad-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46fad-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46fad-123">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="46fad-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46fad-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46fad-124">Header files</span></span>

<span data-ttu-id="46fad-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="46fad-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="46fad-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="46fad-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="46fad-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="46fad-127">Mapitags.h</span></span>
  
> <span data-ttu-id="46fad-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="46fad-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46fad-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="46fad-129">See also</span></span>



[<span data-ttu-id="46fad-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46fad-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46fad-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="46fad-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46fad-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="46fad-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46fad-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="46fad-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

