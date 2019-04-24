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
ms.openlocfilehash: 7dc8ea74d36dd8aee4acec426e97d8b5e3ba2234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278747"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="aae5f-103">Propriedade canônica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="aae5f-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="aae5f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aae5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aae5f-105">Contém o identificador de entrada exclusivo do repositório de mensagens em que um objeto reside.</span><span class="sxs-lookup"><span data-stu-id="aae5f-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aae5f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="aae5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aae5f-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aae5f-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="aae5f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="aae5f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aae5f-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="aae5f-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="aae5f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="aae5f-110">Data type:</span></span>  <br/> |<span data-ttu-id="aae5f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aae5f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aae5f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="aae5f-112">Area:</span></span>  <br/> |<span data-ttu-id="aae5f-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="aae5f-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aae5f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aae5f-114">Remarks</span></span>

<span data-ttu-id="aae5f-115">Essa propriedade é usada para abrir um repositório de mensagens com o método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="aae5f-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="aae5f-116">Também é usado para abrir qualquer objeto pertencente ao repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="aae5f-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="aae5f-117">Para um repositório de mensagens, essa propriedade é idêntica à propriedade do próprio repositório **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aae5f-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="aae5f-118">Um aplicativo cliente pode comparar as duas propriedades usando o método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="aae5f-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aae5f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="aae5f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aae5f-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="aae5f-120">Protocol specifications</span></span>

<span data-ttu-id="aae5f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae5f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aae5f-122">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="aae5f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aae5f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae5f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aae5f-124">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="aae5f-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="aae5f-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae5f-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aae5f-126">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="aae5f-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="aae5f-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae5f-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aae5f-128">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="aae5f-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="aae5f-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae5f-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aae5f-130">Compartilha pastas de caixa de correio entre os clientes.</span><span class="sxs-lookup"><span data-stu-id="aae5f-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aae5f-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aae5f-131">Header files</span></span>

<span data-ttu-id="aae5f-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="aae5f-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="aae5f-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="aae5f-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="aae5f-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="aae5f-134">Mapitags.h</span></span>
  
> <span data-ttu-id="aae5f-135">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="aae5f-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aae5f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="aae5f-136">See also</span></span>



[<span data-ttu-id="aae5f-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="aae5f-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aae5f-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="aae5f-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aae5f-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="aae5f-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aae5f-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="aae5f-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

