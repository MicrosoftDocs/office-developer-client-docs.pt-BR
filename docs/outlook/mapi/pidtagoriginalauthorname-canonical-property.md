---
title: Propriedade canônica PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355773"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="2aa8b-103">Propriedade canônica PidTagOriginalAuthorName</span><span class="sxs-lookup"><span data-stu-id="2aa8b-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="2aa8b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aa8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aa8b-105">Contém o nome de exibição do autor da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2aa8b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2aa8b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2aa8b-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="2aa8b-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="2aa8b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2aa8b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2aa8b-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="2aa8b-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="2aa8b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2aa8b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2aa8b-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="2aa8b-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="2aa8b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2aa8b-112">Area:</span></span>  <br/> |<span data-ttu-id="2aa8b-113">Email</span><span class="sxs-lookup"><span data-stu-id="2aa8b-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2aa8b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aa8b-114">Remarks</span></span>

<span data-ttu-id="2aa8b-115">Essas propriedades são exemplos das propriedades de endereço para o autor de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="2aa8b-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essas propriedades com o valor de **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2aa8b-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="2aa8b-117">Ela nunca é alterada quando a mensagem é encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="2aa8b-118">As propriedades de autor originais permitem a preservação de informações de fora do domínio de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="2aa8b-119">Quando uma mensagem chega de outro domínio de mensagens, como a partir da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não sejam perdidas.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2aa8b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2aa8b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2aa8b-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="2aa8b-121">Protocol specifications</span></span>

<span data-ttu-id="2aa8b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2aa8b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2aa8b-123">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2aa8b-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2aa8b-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2aa8b-125">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2aa8b-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2aa8b-126">Header files</span></span>

<span data-ttu-id="2aa8b-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2aa8b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2aa8b-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="2aa8b-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2aa8b-129">Mapitags.h</span></span>
  
> <span data-ttu-id="2aa8b-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2aa8b-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2aa8b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2aa8b-131">See also</span></span>



[<span data-ttu-id="2aa8b-132">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="2aa8b-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="2aa8b-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2aa8b-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2aa8b-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2aa8b-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2aa8b-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2aa8b-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2aa8b-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2aa8b-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

