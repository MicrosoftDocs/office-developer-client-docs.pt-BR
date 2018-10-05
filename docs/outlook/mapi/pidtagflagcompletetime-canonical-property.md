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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387129"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="55aec-103">Propriedade canônica PidTagFlagCompleteTime</span><span class="sxs-lookup"><span data-stu-id="55aec-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="55aec-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55aec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55aec-105">Especifica a data e hora em tempo Universal Coordenado (UTC) que o objeto de mensagem foi sinalizado como concluída.</span><span class="sxs-lookup"><span data-stu-id="55aec-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55aec-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="55aec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55aec-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="55aec-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="55aec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="55aec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55aec-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="55aec-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="55aec-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="55aec-110">Data type:</span></span>  <br/> |<span data-ttu-id="55aec-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="55aec-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="55aec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="55aec-112">Area:</span></span>  <br/> |<span data-ttu-id="55aec-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="55aec-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55aec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="55aec-114">Remarks</span></span>

<span data-ttu-id="55aec-115">Essa propriedade é excluída se o objeto de mensagem não foi sinalizado completa.</span><span class="sxs-lookup"><span data-stu-id="55aec-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="55aec-116">Resolução menor do tempo deve ser minutos (o valor deve ser um múltiplo de 600,000,000).</span><span class="sxs-lookup"><span data-stu-id="55aec-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="55aec-117">Essa propriedade não deve existir se o objeto é um objeto de reuniões, e ele não deve existir em um objeto task.</span><span class="sxs-lookup"><span data-stu-id="55aec-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55aec-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55aec-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55aec-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="55aec-119">Protocol specifications</span></span>

<span data-ttu-id="55aec-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55aec-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55aec-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="55aec-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55aec-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55aec-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55aec-123">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="55aec-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55aec-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="55aec-124">Header files</span></span>

<span data-ttu-id="55aec-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55aec-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="55aec-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="55aec-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="55aec-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55aec-127">Mapitags.h</span></span>
  
> <span data-ttu-id="55aec-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="55aec-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55aec-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="55aec-129">See also</span></span>



[<span data-ttu-id="55aec-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55aec-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55aec-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="55aec-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55aec-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="55aec-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55aec-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="55aec-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

