---
title: Propriedade canônica PidTagStoreRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d6f858a9f1d3d4620a86621e3f5ecb4ad4609691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278726"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="9b991-103">Propriedade canônica PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="9b991-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="9b991-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b991-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b991-105">Contém o identificador binário exclusivo (chave de registro) do armazenamento de mensagens no qual um objeto reside.</span><span class="sxs-lookup"><span data-stu-id="9b991-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b991-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9b991-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b991-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="9b991-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="9b991-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b991-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b991-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="9b991-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="9b991-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9b991-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b991-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9b991-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9b991-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9b991-112">Area:</span></span>  <br/> |<span data-ttu-id="9b991-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="9b991-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b991-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b991-114">Remarks</span></span>

<span data-ttu-id="9b991-115">Para um armazenamento de mensagens, essa propriedade é idêntica à propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) do próprio armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9b991-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="9b991-116">A relação entre essa propriedade **e PR_RECORD_KEY** é a mesma que a relação entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9b991-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9b991-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b991-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b991-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9b991-118">Protocol specifications</span></span>

<span data-ttu-id="9b991-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b991-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b991-120">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="9b991-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9b991-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b991-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b991-122">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="9b991-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b991-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="9b991-123">Header files</span></span>

<span data-ttu-id="9b991-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b991-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b991-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b991-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b991-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b991-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9b991-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9b991-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b991-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b991-128">See also</span></span>



[<span data-ttu-id="9b991-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b991-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b991-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9b991-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b991-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b991-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b991-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9b991-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

