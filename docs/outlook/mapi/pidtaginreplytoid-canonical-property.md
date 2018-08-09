---
title: Propriedade canônica PidTagInReplyToId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInReplyToId
api_type:
- HeaderDef
ms.assetid: d435a65a-de01-4fb0-bc54-a87a2c4462ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2e8ed4af81de6e48af3e427f2d2d2f94572d241f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769349"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="d2034-103">Propriedade canônica PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="d2034-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="d2034-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2034-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2034-105">Contém o valor da propriedade **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="d2034-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2034-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d2034-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2034-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="d2034-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="d2034-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d2034-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2034-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="d2034-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="d2034-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d2034-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2034-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d2034-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d2034-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d2034-112">Area:</span></span>  <br/> |<span data-ttu-id="d2034-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="d2034-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2034-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2034-114">Remarks</span></span>

<span data-ttu-id="d2034-115">Essas propriedades devem ser definidas em todas as respostas da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2034-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d2034-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2034-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2034-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d2034-117">Protocol specifications</span></span>

<span data-ttu-id="d2034-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2034-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2034-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d2034-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2034-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2034-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2034-121">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d2034-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="d2034-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2034-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2034-123">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2034-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2034-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d2034-124">Header files</span></span>

<span data-ttu-id="d2034-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2034-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2034-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d2034-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2034-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2034-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d2034-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d2034-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2034-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2034-129">See also</span></span>



[<span data-ttu-id="d2034-130">Propriedade canônica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="d2034-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="d2034-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d2034-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2034-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d2034-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2034-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d2034-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2034-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d2034-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

