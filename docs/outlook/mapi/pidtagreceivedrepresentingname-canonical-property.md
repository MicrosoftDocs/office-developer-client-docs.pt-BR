---
title: Propriedade canônica PidTagReceivedRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingName
api_type:
- COM
ms.assetid: 8f699782-8a82-4834-bc55-a0b3cf18a117
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5fce7e6d2163bdb8d1682dbef10d627b34ddd889
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356732"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="13f51-103">Propriedade canônica PidTagReceivedRepresentingName</span><span class="sxs-lookup"><span data-stu-id="13f51-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="13f51-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13f51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13f51-105">Contém o nome de exibição do usuário de mensagens representado pelo usuário receptor.</span><span class="sxs-lookup"><span data-stu-id="13f51-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13f51-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="13f51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13f51-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="13f51-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="13f51-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="13f51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13f51-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="13f51-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="13f51-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="13f51-110">Data type:</span></span>  <br/> |<span data-ttu-id="13f51-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="13f51-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="13f51-112">Área:</span><span class="sxs-lookup"><span data-stu-id="13f51-112">Area:</span></span>  <br/> |<span data-ttu-id="13f51-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="13f51-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13f51-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="13f51-114">Remarks</span></span>

<span data-ttu-id="13f51-115">Essas propriedades são exemplos das propriedades de endereço do usuário de mensagens que está sendo representado pelo usuário receptor.</span><span class="sxs-lookup"><span data-stu-id="13f51-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="13f51-116">Eles devem ser definidos pelo provedor de transporte de entrada, que também é responsável pela autorização ou verificação do representante.</span><span class="sxs-lookup"><span data-stu-id="13f51-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="13f51-117">Se nenhum usuário de mensagens estiver sendo representado, essas propriedades deverão ser definidas como o nome de exibição contido na **propriedade PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="13f51-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="13f51-118">Um aplicativo cliente respondendo a uma mensagem recebida em nome de outro cliente deve copiar essas propriedades da mensagem recebida para a propriedade **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) da resposta.</span><span class="sxs-lookup"><span data-stu-id="13f51-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13f51-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="13f51-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13f51-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="13f51-120">Protocol specifications</span></span>

<span data-ttu-id="13f51-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f51-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f51-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13f51-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13f51-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f51-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f51-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="13f51-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="13f51-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f51-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f51-126">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="13f51-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="13f51-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f51-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f51-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="13f51-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="13f51-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f51-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f51-130">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="13f51-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="13f51-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13f51-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13f51-132">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.</span><span class="sxs-lookup"><span data-stu-id="13f51-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13f51-133">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="13f51-133">Header files</span></span>

<span data-ttu-id="13f51-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13f51-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="13f51-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="13f51-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="13f51-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13f51-136">Mapitags.h</span></span>
  
> <span data-ttu-id="13f51-137">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="13f51-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13f51-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="13f51-138">See also</span></span>



[<span data-ttu-id="13f51-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13f51-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13f51-140">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="13f51-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13f51-141">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="13f51-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13f51-142">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="13f51-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

