---
title: Propriedade canônica PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cae4ef6e4d7634ca2b429eb946aa948f5d90cd92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770164"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="5d605-103">Propriedade canônica PidTagToDoItemFlags</span><span class="sxs-lookup"><span data-stu-id="5d605-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5d605-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d605-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d605-105">Representa a condição de um item de tarefas pendentes sinalizadas.</span><span class="sxs-lookup"><span data-stu-id="5d605-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d605-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5d605-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d605-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5d605-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5d605-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5d605-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d605-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="5d605-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="5d605-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5d605-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d605-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5d605-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5d605-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5d605-112">Area:</span></span>  <br/> |<span data-ttu-id="5d605-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="5d605-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d605-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d605-114">Remarks</span></span>

<span data-ttu-id="5d605-115">Essa propriedade é um campo de bit no qual cada bit deve ser definido como 1 se se aplica a condição associada na tabela a seguir, caso contrário 0.</span><span class="sxs-lookup"><span data-stu-id="5d605-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="5d605-116">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="5d605-116">Numeric value</span></span>  <br/> |<span data-ttu-id="5d605-117">Nome</span><span class="sxs-lookup"><span data-stu-id="5d605-117">Name</span></span>  <br/> |<span data-ttu-id="5d605-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d605-118">Description</span></span>  <br/> |
|<span data-ttu-id="5d605-119">Não estiver presente</span><span class="sxs-lookup"><span data-stu-id="5d605-119">Not present</span></span>  <br/> |<span data-ttu-id="5d605-120">N/A</span><span class="sxs-lookup"><span data-stu-id="5d605-120">N/A</span></span>  <br/> |<span data-ttu-id="5d605-121">Sem sinalizador</span><span class="sxs-lookup"><span data-stu-id="5d605-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="5d605-122">1</span><span class="sxs-lookup"><span data-stu-id="5d605-122">1</span></span>  <br/> |<span data-ttu-id="5d605-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="5d605-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="5d605-124">Objeto é o tempo sinalizado</span><span class="sxs-lookup"><span data-stu-id="5d605-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="5d605-125">8</span><span class="sxs-lookup"><span data-stu-id="5d605-125">8</span></span>  <br/> |<span data-ttu-id="5d605-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="5d605-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="5d605-127">Só deve ser definido em um objeto de mensagem de rascunho e significa que o objeto foi sinalizado para destinatários.</span><span class="sxs-lookup"><span data-stu-id="5d605-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="5d605-128">Todos os bits que não forem especificados na tabela são reservados.</span><span class="sxs-lookup"><span data-stu-id="5d605-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="5d605-129">Eles devem ser ignorados, mas devem ser preservados se eles estiverem definidos.</span><span class="sxs-lookup"><span data-stu-id="5d605-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d605-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d605-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d605-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5d605-131">Protocol specifications</span></span>

<span data-ttu-id="5d605-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d605-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d605-133">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5d605-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d605-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d605-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d605-135">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="5d605-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d605-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d605-136">Header files</span></span>

<span data-ttu-id="5d605-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d605-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d605-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5d605-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d605-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d605-139">Mapitags.h</span></span>
  
> <span data-ttu-id="5d605-140">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5d605-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d605-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d605-141">See also</span></span>



[<span data-ttu-id="5d605-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5d605-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d605-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5d605-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d605-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5d605-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d605-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5d605-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

