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
ms.openlocfilehash: e5b283376d018b7b2675e05f994d586126437590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769544"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="0015a-103">Propriedade canônica PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="0015a-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="0015a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0015a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0015a-105">Contém a chave de pesquisa do autor da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="0015a-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0015a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0015a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0015a-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="0015a-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="0015a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0015a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0015a-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="0015a-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="0015a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0015a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0015a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0015a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0015a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0015a-112">Area:</span></span>  <br/> |<span data-ttu-id="0015a-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="0015a-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0015a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0015a-114">Remarks</span></span>

<span data-ttu-id="0015a-115">Essa propriedade é uma das propriedades de endereço para o autor de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="0015a-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="0015a-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade como o valor da propriedade[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_SEARCH_KEY**.</span><span class="sxs-lookup"><span data-stu-id="0015a-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="0015a-117">Ele nunca é alterado quando a mensagem for encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="0015a-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="0015a-118">As propriedades de autor original permitem preservação de informações de fora do domínio de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="0015a-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="0015a-119">Quando uma mensagem é recebida de outro domínio de mensagens, como da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não sejam perdidas.</span><span class="sxs-lookup"><span data-stu-id="0015a-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0015a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0015a-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0015a-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0015a-121">Header files</span></span>

<span data-ttu-id="0015a-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0015a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0015a-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0015a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0015a-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0015a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0015a-125">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="0015a-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0015a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0015a-126">See also</span></span>



[<span data-ttu-id="0015a-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0015a-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0015a-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0015a-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0015a-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0015a-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0015a-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0015a-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

