---
title: Propriedade canônica PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425586"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="5b406-103">Propriedade canônica PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="5b406-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5b406-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b406-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b406-105">Contém o identificador de entrada do autor da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="5b406-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b406-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5b406-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b406-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5b406-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5b406-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5b406-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b406-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="5b406-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="5b406-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5b406-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b406-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5b406-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5b406-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5b406-112">Area:</span></span>  <br/> |<span data-ttu-id="5b406-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="5b406-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b406-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b406-114">Remarks</span></span>

<span data-ttu-id="5b406-115">Essa propriedade é uma das propriedades de endereço para o autor de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5b406-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="5b406-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade com o valor de **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5b406-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="5b406-117">Ela nunca é alterada quando a mensagem é encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="5b406-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="5b406-118">A propriedade Author original permite preservar as informações de fora do domínio de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="5b406-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="5b406-119">Quando uma mensagem chega de outro domínio de mensagens, como a partir da Internet, essa propriedade oferece uma maneira de garantir que as informações originais não sejam perdidas.</span><span class="sxs-lookup"><span data-stu-id="5b406-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b406-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b406-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5b406-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5b406-121">Header files</span></span>

<span data-ttu-id="5b406-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5b406-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b406-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5b406-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b406-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5b406-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5b406-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5b406-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b406-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b406-126">See also</span></span>



[<span data-ttu-id="5b406-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b406-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b406-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5b406-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b406-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b406-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b406-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5b406-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

