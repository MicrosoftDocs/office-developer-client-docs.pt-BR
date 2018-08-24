---
title: Propriedade canônica PidTagStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ffe4798c5e8ef200619b060a58e868cc4a1b2bc2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590068"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="8b434-103">Propriedade canônica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="8b434-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8b434-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b434-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b434-105">Contém o identificador exclusivo de entrada do repositório de mensagem em que reside a um objeto.</span><span class="sxs-lookup"><span data-stu-id="8b434-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b434-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8b434-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b434-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8b434-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8b434-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8b434-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b434-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="8b434-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="8b434-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8b434-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b434-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8b434-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8b434-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8b434-112">Area:</span></span>  <br/> |<span data-ttu-id="8b434-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="8b434-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b434-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b434-114">Remarks</span></span>

<span data-ttu-id="8b434-115">Essa propriedade é usada para abrir um armazenamento de mensagens com o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="8b434-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="8b434-116">Ele também é usado para abrir qualquer objeto que pertence o armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b434-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="8b434-117">Para um armazenamento de mensagens, essa propriedade é idêntica à propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do repositório.</span><span class="sxs-lookup"><span data-stu-id="8b434-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="8b434-118">Um aplicativo cliente pode comparar as duas propriedades usando o método [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="8b434-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b434-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b434-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b434-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8b434-120">Protocol specifications</span></span>

<span data-ttu-id="8b434-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b434-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b434-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8b434-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b434-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b434-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b434-124">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="8b434-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8b434-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b434-125">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b434-126">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="8b434-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8b434-127">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b434-127">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b434-128">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="8b434-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="8b434-129">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b434-129">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b434-130">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="8b434-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b434-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8b434-131">Header files</span></span>

<span data-ttu-id="8b434-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b434-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b434-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8b434-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b434-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b434-134">Mapitags.h</span></span>
  
> <span data-ttu-id="8b434-135">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8b434-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b434-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b434-136">See also</span></span>



[<span data-ttu-id="8b434-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8b434-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b434-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8b434-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b434-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8b434-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b434-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8b434-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

