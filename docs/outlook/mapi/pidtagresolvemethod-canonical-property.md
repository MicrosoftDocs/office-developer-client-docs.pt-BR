---
title: Propriedade canônica PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331399"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="3147b-103">Propriedade canônica PidTagResolveMethod</span><span class="sxs-lookup"><span data-stu-id="3147b-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="3147b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3147b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3147b-105">Contém o valor de resolução de conflitos de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="3147b-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3147b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3147b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3147b-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="3147b-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="3147b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3147b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3147b-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="3147b-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="3147b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3147b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3147b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3147b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3147b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3147b-112">Area:</span></span>  <br/> |<span data-ttu-id="3147b-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="3147b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3147b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3147b-114">Remarks</span></span>

<span data-ttu-id="3147b-115">Essa propriedade na pasta que contém a mensagem de resolução de conflitos indicará como resolver o conflito.</span><span class="sxs-lookup"><span data-stu-id="3147b-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="3147b-116">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="3147b-116">This property is not required.</span></span> <span data-ttu-id="3147b-117">No entanto, se estiver definido, sinalizadores que não sejam os seguintes não devem estar presentes:</span><span class="sxs-lookup"><span data-stu-id="3147b-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3147b-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="3147b-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="3147b-119">A mensagem de resolução de conflitos deve ser gerada.</span><span class="sxs-lookup"><span data-stu-id="3147b-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="3147b-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="3147b-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="3147b-121">Substituir a mensagem de destino com as alterações atuais aplicadas.</span><span class="sxs-lookup"><span data-stu-id="3147b-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="3147b-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="3147b-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="3147b-123">Não envie mensagem de notificação de conflito ao gerar mensagem de resolução de conflito na pasta pública.</span><span class="sxs-lookup"><span data-stu-id="3147b-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="3147b-124">Um cliente ou servidor não deve gerar uma mensagem de resolução de conflito para mensagens associadas.</span><span class="sxs-lookup"><span data-stu-id="3147b-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="3147b-125">Essas mensagens devem ser resolvidas usando **RESOLVE_METHOD_LAST_WRITER_WINS** semântica.</span><span class="sxs-lookup"><span data-stu-id="3147b-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3147b-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3147b-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3147b-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3147b-127">Protocol specifications</span></span>

<span data-ttu-id="3147b-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3147b-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3147b-129">Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="3147b-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="3147b-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3147b-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3147b-131">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="3147b-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3147b-132">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3147b-132">Header files</span></span>

<span data-ttu-id="3147b-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3147b-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="3147b-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3147b-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="3147b-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3147b-135">Mapitags.h</span></span>
  
> <span data-ttu-id="3147b-136">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3147b-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3147b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3147b-137">See also</span></span>



[<span data-ttu-id="3147b-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3147b-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3147b-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3147b-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3147b-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3147b-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3147b-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3147b-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

