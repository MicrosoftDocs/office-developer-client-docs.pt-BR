---
title: Propriedade canônico de PidTagStoreRecordKey
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 4598ca5e654308f7701b1dd66adb227599773b7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770101"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="c3114-103">Propriedade canônico de PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="c3114-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="c3114-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3114-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3114-105">Contém o identificador binário-comparável exclusivo (chave de registro) o armazenamento de mensagens em que um objeto reside.</span><span class="sxs-lookup"><span data-stu-id="c3114-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3114-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c3114-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3114-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="c3114-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="c3114-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c3114-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3114-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="c3114-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="c3114-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c3114-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3114-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c3114-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c3114-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c3114-112">Area:</span></span>  <br/> |<span data-ttu-id="c3114-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="c3114-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3114-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c3114-114">Remarks</span></span>

<span data-ttu-id="c3114-115">Para um armazenamento de mensagens, essa propriedade é idêntica à propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) do repositório.</span><span class="sxs-lookup"><span data-stu-id="c3114-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c3114-116">A relação entre essa propriedade e **PR_RECORD_KEY** é o mesmo que a relação entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c3114-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c3114-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3114-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3114-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c3114-118">Protocol specifications</span></span>

<span data-ttu-id="c3114-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3114-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3114-120">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="c3114-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c3114-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3114-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3114-122">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="c3114-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3114-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c3114-123">Header files</span></span>

<span data-ttu-id="c3114-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3114-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3114-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c3114-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3114-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c3114-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c3114-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c3114-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3114-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3114-128">See also</span></span>



[<span data-ttu-id="c3114-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c3114-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3114-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c3114-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3114-131">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c3114-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3114-132">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="c3114-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

