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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342508"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="c0bc1-103">Propriedade canônica PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="c0bc1-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c0bc1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0bc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0bc1-105">Contém o identificador de entrada da pasta onde a mensagem deve ser movida após o envio.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0bc1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c0bc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0bc1-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c0bc1-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c0bc1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c0bc1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0bc1-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="c0bc1-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="c0bc1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c0bc1-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0bc1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c0bc1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c0bc1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c0bc1-112">Area:</span></span>  <br/> |<span data-ttu-id="c0bc1-113">MAPI não-transmittable</span><span class="sxs-lookup"><span data-stu-id="c0bc1-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0bc1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0bc1-114">Remarks</span></span>

<span data-ttu-id="c0bc1-115">Essa propriedade é freqüentemente copiada da propriedade **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)), a pasta Itens enviados padrão do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="c0bc1-116">O aplicativo cliente usa essa propriedade com a propriedade **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para controlar o que acontece a uma mensagem após ele ser enviado.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="c0bc1-117">Um deles deve ser definido, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c0bc1-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0bc1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0bc1-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="c0bc1-119">Protocol specifications</span></span>

<span data-ttu-id="c0bc1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0bc1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0bc1-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0bc1-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0bc1-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0bc1-123">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c0bc1-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0bc1-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0bc1-125">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0bc1-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c0bc1-126">Header files</span></span>

<span data-ttu-id="c0bc1-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c0bc1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0bc1-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0bc1-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c0bc1-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c0bc1-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c0bc1-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0bc1-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0bc1-131">See also</span></span>



[<span data-ttu-id="c0bc1-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c0bc1-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0bc1-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c0bc1-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0bc1-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c0bc1-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0bc1-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c0bc1-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

