---
title: Propriedade canônica PidTagOriginalSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2aa0a8601a72b6d4c40167ac55d3d643bf946708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769573"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="bd9fe-103">Propriedade canônica PidTagOriginalSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="bd9fe-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="bd9fe-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd9fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd9fe-105">Contém a chave de pesquisa para o remetente da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd9fe-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bd9fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd9fe-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bd9fe-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="bd9fe-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bd9fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd9fe-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="bd9fe-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="bd9fe-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bd9fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd9fe-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd9fe-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bd9fe-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bd9fe-112">Area:</span></span>  <br/> |<span data-ttu-id="bd9fe-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="bd9fe-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd9fe-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd9fe-114">Remarks</span></span>

<span data-ttu-id="bd9fe-115">Essa propriedade é uma das propriedades de endereço do remetente original de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="bd9fe-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade como o valor da propriedade **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bd9fe-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="bd9fe-117">Ele nunca é alterado quando a mensagem for encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd9fe-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd9fe-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd9fe-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bd9fe-119">Protocol specifications</span></span>

<span data-ttu-id="bd9fe-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd9fe-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd9fe-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd9fe-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd9fe-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd9fe-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd9fe-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd9fe-124">Header files</span></span>

<span data-ttu-id="bd9fe-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd9fe-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd9fe-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd9fe-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd9fe-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bd9fe-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd9fe-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd9fe-129">See also</span></span>



[<span data-ttu-id="bd9fe-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bd9fe-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd9fe-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bd9fe-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd9fe-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bd9fe-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd9fe-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bd9fe-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

