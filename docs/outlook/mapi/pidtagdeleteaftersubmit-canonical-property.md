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
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359910"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="a5051-103">Propriedade canônica PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="a5051-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="a5051-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5051-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5051-105">Contém TRUE se um aplicativo cliente deseja que o MAPI exclua a mensagem associada após o envio.</span><span class="sxs-lookup"><span data-stu-id="a5051-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5051-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a5051-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5051-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="a5051-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="a5051-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a5051-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5051-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="a5051-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="a5051-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a5051-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5051-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a5051-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a5051-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a5051-112">Area:</span></span>  <br/> |<span data-ttu-id="a5051-113">MAPI não-transmittable</span><span class="sxs-lookup"><span data-stu-id="a5051-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5051-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5051-114">Remarks</span></span>

<span data-ttu-id="a5051-115">Um aplicativo cliente usa essa propriedade com a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para controlar o que acontece a uma mensagem após ele ser enviado.</span><span class="sxs-lookup"><span data-stu-id="a5051-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="a5051-116">Um deles deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="a5051-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a5051-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5051-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5051-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="a5051-118">Protocol specifications</span></span>

<span data-ttu-id="a5051-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5051-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5051-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5051-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5051-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5051-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5051-122">Especifica operações permitidas para os principais objetos do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5051-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="a5051-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5051-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5051-124">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a5051-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5051-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a5051-125">Header files</span></span>

<span data-ttu-id="a5051-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a5051-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5051-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a5051-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5051-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a5051-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a5051-129">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="a5051-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5051-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5051-130">See also</span></span>



[<span data-ttu-id="a5051-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a5051-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5051-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a5051-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5051-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a5051-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5051-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a5051-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

