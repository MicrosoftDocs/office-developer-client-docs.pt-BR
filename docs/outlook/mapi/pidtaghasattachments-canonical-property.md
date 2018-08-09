---
title: Propriedade canônica PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3b618e5a79c3b7e3810ea541aa9b905dfa4188a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769292"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="be7f1-103">Propriedade canônica PidTagHasAttachments</span><span class="sxs-lookup"><span data-stu-id="be7f1-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="be7f1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be7f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be7f1-105">Conterá TRUE se uma mensagem contém pelo menos um anexo.</span><span class="sxs-lookup"><span data-stu-id="be7f1-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be7f1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="be7f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be7f1-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="be7f1-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="be7f1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be7f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be7f1-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="be7f1-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="be7f1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="be7f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="be7f1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="be7f1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="be7f1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="be7f1-112">Area:</span></span>  <br/> |<span data-ttu-id="be7f1-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="be7f1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be7f1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be7f1-114">Remarks</span></span>

<span data-ttu-id="be7f1-115">O armazenamento de mensagens copia essa propriedade do sinalizador **MSGFLAG_HASATTACH** da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="be7f1-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="be7f1-116">Um aplicativo cliente pode usar **PR_HASATTACH** para classificar os anexos de mensagens em um visualizador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="be7f1-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="be7f1-117">O valor que dessa propriedade é atualizada com o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="be7f1-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="be7f1-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="be7f1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be7f1-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="be7f1-119">Protocol specifications</span></span>

<span data-ttu-id="be7f1-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be7f1-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be7f1-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="be7f1-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be7f1-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="be7f1-122">Header files</span></span>

<span data-ttu-id="be7f1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be7f1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="be7f1-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="be7f1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="be7f1-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be7f1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="be7f1-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="be7f1-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be7f1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="be7f1-127">See also</span></span>



[<span data-ttu-id="be7f1-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="be7f1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be7f1-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="be7f1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be7f1-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="be7f1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be7f1-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="be7f1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

