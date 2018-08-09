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
ms.openlocfilehash: 4b2f47f503caa32a1bdcd287e2fa5e894d667573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769541"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="7273c-103">Propriedade canônica PidTagOriginalAuthorName</span><span class="sxs-lookup"><span data-stu-id="7273c-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="7273c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7273c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7273c-105">Contém o nome de exibição do autor da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="7273c-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7273c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7273c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7273c-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="7273c-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="7273c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7273c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7273c-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="7273c-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="7273c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7273c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7273c-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7273c-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7273c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7273c-112">Area:</span></span>  <br/> |<span data-ttu-id="7273c-113">Email</span><span class="sxs-lookup"><span data-stu-id="7273c-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7273c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7273c-114">Remarks</span></span>

<span data-ttu-id="7273c-115">Essas propriedades são exemplos das propriedades de endereço para o autor de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7273c-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="7273c-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essas propriedades para o valor da **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7273c-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="7273c-117">Ele nunca é alterado quando a mensagem for encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="7273c-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="7273c-118">As propriedades de autor original permitem preservação de informações de fora do domínio de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="7273c-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="7273c-119">Quando uma mensagem é recebida de outro domínio de mensagens, como da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não sejam perdidas.</span><span class="sxs-lookup"><span data-stu-id="7273c-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7273c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7273c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7273c-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7273c-121">Protocol specifications</span></span>

<span data-ttu-id="7273c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7273c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7273c-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7273c-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7273c-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7273c-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7273c-125">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="7273c-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7273c-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7273c-126">Header files</span></span>

<span data-ttu-id="7273c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7273c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7273c-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7273c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="7273c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7273c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="7273c-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7273c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7273c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7273c-131">See also</span></span>



[<span data-ttu-id="7273c-132">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="7273c-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="7273c-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7273c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7273c-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7273c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7273c-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7273c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7273c-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7273c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

