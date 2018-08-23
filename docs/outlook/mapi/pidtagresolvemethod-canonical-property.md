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
ms.openlocfilehash: e67cbb113899487f489ef7235d92d1adfcb76163
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563636"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="fccea-103">Propriedade canônica PidTagResolveMethod</span><span class="sxs-lookup"><span data-stu-id="fccea-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="fccea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fccea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fccea-105">Contém o valor de resolução de conflito de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="fccea-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fccea-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fccea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fccea-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="fccea-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="fccea-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fccea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fccea-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="fccea-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="fccea-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fccea-110">Data type:</span></span>  <br/> |<span data-ttu-id="fccea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fccea-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fccea-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fccea-112">Area:</span></span>  <br/> |<span data-ttu-id="fccea-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="fccea-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fccea-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fccea-114">Remarks</span></span>

<span data-ttu-id="fccea-115">Essa propriedade na pasta que contém a mensagem de resolução de conflito indicará como resolver o conflito.</span><span class="sxs-lookup"><span data-stu-id="fccea-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="fccea-116">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="fccea-116">This property is not required.</span></span> <span data-ttu-id="fccea-117">No entanto, se ele estiver definido, os sinalizadores que não seja a seguir não devem estar presentes:</span><span class="sxs-lookup"><span data-stu-id="fccea-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fccea-118">RESOLVE_METHOD_DEFAULT (0X00000000)</span><span class="sxs-lookup"><span data-stu-id="fccea-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="fccea-119">Conflito resolver mensagem deve ser gerada.</span><span class="sxs-lookup"><span data-stu-id="fccea-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="fccea-120">RESOLVE_METHOD_LAST_WRITER_WINS (0X00000001)</span><span class="sxs-lookup"><span data-stu-id="fccea-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="fccea-121">Substitua a mensagem de destino com alterações atuais que está sendo aplicadas.</span><span class="sxs-lookup"><span data-stu-id="fccea-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="fccea-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0X00000002)</span><span class="sxs-lookup"><span data-stu-id="fccea-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="fccea-123">Não envie mensagem de notificação de conflito quando gerando conflito resolver a mensagem na pasta pública.</span><span class="sxs-lookup"><span data-stu-id="fccea-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="fccea-124">Um cliente ou servidor não deve gerar uma mensagem de conflito resolve para mensagens associadas.</span><span class="sxs-lookup"><span data-stu-id="fccea-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="fccea-125">Essas mensagens devem ser resolvidas usando semântica **RESOLVE_METHOD_LAST_WRITER_WINS** .</span><span class="sxs-lookup"><span data-stu-id="fccea-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fccea-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fccea-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fccea-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fccea-127">Protocol specifications</span></span>

<span data-ttu-id="fccea-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fccea-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fccea-129">Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="fccea-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="fccea-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fccea-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fccea-131">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="fccea-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fccea-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fccea-132">Header files</span></span>

<span data-ttu-id="fccea-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fccea-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="fccea-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fccea-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="fccea-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fccea-135">Mapitags.h</span></span>
  
> <span data-ttu-id="fccea-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fccea-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fccea-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="fccea-137">See also</span></span>



[<span data-ttu-id="fccea-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fccea-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fccea-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fccea-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fccea-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fccea-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fccea-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fccea-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

