---
title: Propriedade canônica PidTagOriginalAuthorEntryId Canonical Property
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
ms.openlocfilehash: 03244fb240231a105b0a25a0797c13b9bf7f7a80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769535"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="aa34f-103">Propriedade canônica PidTagOriginalAuthorEntryId Canonical Property</span><span class="sxs-lookup"><span data-stu-id="aa34f-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="aa34f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa34f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa34f-105">Contém o identificador de entrada do autor da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="aa34f-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa34f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="aa34f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa34f-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="aa34f-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="aa34f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="aa34f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa34f-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="aa34f-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="aa34f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="aa34f-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa34f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aa34f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aa34f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="aa34f-112">Area:</span></span>  <br/> |<span data-ttu-id="aa34f-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="aa34f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa34f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa34f-114">Remarks</span></span>

<span data-ttu-id="aa34f-115">Essa propriedade é uma das propriedades de endereço para o autor de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa34f-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="aa34f-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade como o valor de **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa34f-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="aa34f-117">Ele nunca é alterado quando a mensagem for encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="aa34f-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="aa34f-118">A propriedade autor original permite a preservação de informações de fora do domínio de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="aa34f-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="aa34f-119">Quando uma mensagem é recebida de outro domínio de mensagens, como a Internet, essa propriedade oferece uma maneira de garantir que as informações originais não serão perdido.</span><span class="sxs-lookup"><span data-stu-id="aa34f-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aa34f-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa34f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aa34f-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aa34f-121">Header files</span></span>

<span data-ttu-id="aa34f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa34f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa34f-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="aa34f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa34f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aa34f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="aa34f-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="aa34f-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa34f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa34f-126">See also</span></span>



[<span data-ttu-id="aa34f-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="aa34f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa34f-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="aa34f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa34f-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="aa34f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa34f-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="aa34f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

