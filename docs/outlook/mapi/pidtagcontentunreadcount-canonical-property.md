---
title: Propriedade canônica PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b15dd467b7418ea10d384183dc32284924a90212
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581073"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="3880c-103">Propriedade canônica PidTagContentUnreadCount</span><span class="sxs-lookup"><span data-stu-id="3880c-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="3880c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3880c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3880c-105">Contém o número de mensagens não lidas em uma pasta, como computado pelo armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3880c-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3880c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3880c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3880c-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="3880c-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="3880c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3880c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3880c-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="3880c-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="3880c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3880c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3880c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3880c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3880c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3880c-112">Area:</span></span>  <br/> |<span data-ttu-id="3880c-113">Folder</span><span class="sxs-lookup"><span data-stu-id="3880c-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3880c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3880c-114">Remarks</span></span>

<span data-ttu-id="3880c-115">Essa propriedade computada pelo armazenamento de mensagens é usada para dois diferentes, embora relacionado, fins.</span><span class="sxs-lookup"><span data-stu-id="3880c-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="3880c-116">Em um objeto de pasta MAPI, ele contém o número de mensagens em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="3880c-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="3880c-117">Em uma linha de cabeçalho nas tabelas MAPI categorizadas, ele contém o número de mensagens não lidas não associado na categoria correspondente para essa linha de título.</span><span class="sxs-lookup"><span data-stu-id="3880c-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="3880c-118">Essa propriedade contém o número de mensagens na tabela de conteúdo de pasta para o qual o sinalizador MSGFLAG_READ não está definido na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3880c-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="3880c-119">A propriedade **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contém a contagem total de mensagens para a pasta.</span><span class="sxs-lookup"><span data-stu-id="3880c-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="3880c-120">O **PR_CONTENT_COUNT** e essa propriedade são somente leitura aos clientes.</span><span class="sxs-lookup"><span data-stu-id="3880c-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="3880c-121">Alguns aplicativos cliente exibem a linha do cabeçalho de uma categoria de forma diferente, dependendo do valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="3880c-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="3880c-122">Por exemplo, um cliente pode exibir uma categoria que inclui mensagens não lidas em negrito.</span><span class="sxs-lookup"><span data-stu-id="3880c-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="3880c-123">Essa propriedade não pode ser usada como uma categoria e uma tentativa para isso resulta em que o valor MAPI_E_INVALID_PARAMETER sendo retornado pelo método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="3880c-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3880c-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3880c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3880c-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3880c-125">Protocol specifications</span></span>

<span data-ttu-id="3880c-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3880c-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3880c-127">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3880c-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3880c-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3880c-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3880c-129">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="3880c-129">Handles folder operations.</span></span>
    
<span data-ttu-id="3880c-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3880c-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3880c-131">Inclui as operações permitidas para os objetos de tabela principal.</span><span class="sxs-lookup"><span data-stu-id="3880c-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3880c-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3880c-132">Header files</span></span>

<span data-ttu-id="3880c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3880c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="3880c-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3880c-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="3880c-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3880c-135">Mapitags.h</span></span>
  
> <span data-ttu-id="3880c-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3880c-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3880c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3880c-137">See also</span></span>



[<span data-ttu-id="3880c-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3880c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3880c-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3880c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3880c-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3880c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3880c-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3880c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

