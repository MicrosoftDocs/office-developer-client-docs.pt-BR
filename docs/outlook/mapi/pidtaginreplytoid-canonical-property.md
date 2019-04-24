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
ms.openlocfilehash: 036f38c1228e08cfc9a2093c027195a802904f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358832"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="0e4e8-103">Propriedade canônica PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="0e4e8-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="0e4e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e4e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e4e8-105">Contém o valor da propriedade **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="0e4e8-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e4e8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0e4e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e4e8-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="0e4e8-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="0e4e8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0e4e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e4e8-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="0e4e8-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="0e4e8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0e4e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e4e8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e4e8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0e4e8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0e4e8-112">Area:</span></span>  <br/> |<span data-ttu-id="0e4e8-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="0e4e8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e4e8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e4e8-114">Remarks</span></span>

<span data-ttu-id="0e4e8-115">Essas propriedades devem ser definidas em todas as respostas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0e4e8-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e4e8-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e4e8-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e4e8-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="0e4e8-117">Protocol specifications</span></span>

<span data-ttu-id="0e4e8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e4e8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e4e8-119">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0e4e8-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e4e8-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e4e8-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e4e8-121">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="0e4e8-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="0e4e8-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e4e8-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e4e8-123">Converte as convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0e4e8-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e4e8-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0e4e8-124">Header files</span></span>

<span data-ttu-id="0e4e8-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0e4e8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e4e8-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0e4e8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e4e8-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0e4e8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0e4e8-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0e4e8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e4e8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e4e8-129">See also</span></span>



[<span data-ttu-id="0e4e8-130">Propriedade canônica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="0e4e8-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="0e4e8-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e4e8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e4e8-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0e4e8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e4e8-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0e4e8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e4e8-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0e4e8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

