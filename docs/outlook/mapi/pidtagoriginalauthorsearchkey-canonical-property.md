---
title: Propriedade canônica PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409577"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="2c701-103">Propriedade canônica PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="2c701-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="2c701-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c701-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c701-105">Contém a chave de pesquisa do autor da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="2c701-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c701-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2c701-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c701-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="2c701-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="2c701-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2c701-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c701-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="2c701-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="2c701-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2c701-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c701-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2c701-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2c701-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c701-112">Area:</span></span>  <br/> |<span data-ttu-id="2c701-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="2c701-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c701-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c701-114">Remarks</span></span>

<span data-ttu-id="2c701-115">Essa propriedade é uma das propriedades de endereço do autor de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2c701-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="2c701-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade como o valor da PR_SENDER_SEARCH_KEY[propriedade PidTagSenderSearchKey.](pidtagsendersearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="2c701-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="2c701-117">Ela nunca é alterada quando a mensagem é encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="2c701-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="2c701-118">As propriedades originais do autor permitem a preservação de informações de fora do domínio de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="2c701-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="2c701-119">Quando uma mensagem chega de outro domínio de mensagens, como da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não são perdidas.</span><span class="sxs-lookup"><span data-stu-id="2c701-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c701-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c701-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2c701-121">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="2c701-121">Header files</span></span>

<span data-ttu-id="2c701-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c701-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c701-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2c701-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c701-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c701-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2c701-125">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="2c701-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c701-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c701-126">See also</span></span>



[<span data-ttu-id="2c701-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c701-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c701-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2c701-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c701-129">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2c701-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c701-130">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2c701-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

