---
title: Propriedade canônica PidTagDeleteAfterSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7a63b3ad3c45790e043e1ea8e7d996c4847ef8d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769156"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="b3472-103">Propriedade canônica PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="b3472-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="b3472-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3472-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3472-105">Contém TRUE se quiser que um aplicativo cliente MAPI para excluir a mensagem associada após o envio.</span><span class="sxs-lookup"><span data-stu-id="b3472-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3472-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b3472-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b3472-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="b3472-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="b3472-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b3472-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b3472-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="b3472-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="b3472-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b3472-110">Data type:</span></span>  <br/> |<span data-ttu-id="b3472-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b3472-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b3472-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b3472-112">Area:</span></span>  <br/> |<span data-ttu-id="b3472-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="b3472-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3472-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3472-114">Remarks</span></span>

<span data-ttu-id="b3472-115">Um aplicativo cliente usa essa propriedade com a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para controlar o que acontece a uma mensagem depois que ela é enviada.</span><span class="sxs-lookup"><span data-stu-id="b3472-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="b3472-116">Um ou outro deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="b3472-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b3472-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3472-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b3472-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b3472-118">Protocol specifications</span></span>

<span data-ttu-id="b3472-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3472-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3472-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b3472-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b3472-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3472-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3472-122">Especifica as operações permitidas para os objetos do repositório de mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="b3472-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="b3472-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3472-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3472-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b3472-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b3472-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3472-125">Header files</span></span>

<span data-ttu-id="b3472-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3472-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b3472-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b3472-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b3472-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b3472-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b3472-129">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="b3472-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3472-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3472-130">See also</span></span>



[<span data-ttu-id="b3472-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b3472-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b3472-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b3472-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b3472-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b3472-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b3472-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b3472-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

