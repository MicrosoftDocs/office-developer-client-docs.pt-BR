---
title: Propriedade canônica PidTagSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398805"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="4b4a6-103">Propriedade canônica PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="4b4a6-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4b4a6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b4a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b4a6-105">Contém o identificador de entrada da pasta onde a mensagem deve ser movida após o envio.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b4a6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4b4a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b4a6-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4b4a6-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4b4a6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4b4a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b4a6-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="4b4a6-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="4b4a6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4b4a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b4a6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4b4a6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4b4a6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4b4a6-112">Area:</span></span>  <br/> |<span data-ttu-id="4b4a6-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="4b4a6-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b4a6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b4a6-114">Remarks</span></span>

<span data-ttu-id="4b4a6-115">Essa propriedade normalmente é copiada da propriedade **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)), a pasta de itens enviados padrão do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="4b4a6-116">O aplicativo cliente usa essa propriedade com a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para controlar o que acontece a uma mensagem depois que ela é enviada.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="4b4a6-117">Um ou outro deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b4a6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b4a6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b4a6-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4b4a6-119">Protocol specifications</span></span>

<span data-ttu-id="4b4a6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b4a6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b4a6-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b4a6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b4a6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b4a6-123">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4b4a6-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b4a6-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b4a6-125">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b4a6-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4b4a6-126">Header files</span></span>

<span data-ttu-id="4b4a6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b4a6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b4a6-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b4a6-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4b4a6-129">Mapitags.h</span></span>
  
> <span data-ttu-id="4b4a6-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b4a6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b4a6-131">See also</span></span>



[<span data-ttu-id="4b4a6-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4b4a6-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b4a6-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4b4a6-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b4a6-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4b4a6-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b4a6-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4b4a6-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

