---
title: Propriedade canônica PidTagReceivedRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingSearchKey
api_type:
- COM
ms.assetid: 234c797c-4a3c-4e05-be22-2a2fa377871f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 834e97d8bd7bf31a1241fcf0454594b015902673
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769762"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a><span data-ttu-id="19d9b-103">Propriedade canônica PidTagReceivedRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="19d9b-103">PidTagReceivedRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="19d9b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19d9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19d9b-105">Contém a chave de pesquisa para o usuário mensagens representado pelo usuário receptor.</span><span class="sxs-lookup"><span data-stu-id="19d9b-105">Contains the search key for the messaging user represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19d9b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="19d9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19d9b-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="19d9b-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="19d9b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="19d9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19d9b-109">0x0052</span><span class="sxs-lookup"><span data-stu-id="19d9b-109">0x0052</span></span>  <br/> |
|<span data-ttu-id="19d9b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="19d9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="19d9b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="19d9b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="19d9b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="19d9b-112">Area:</span></span>  <br/> |<span data-ttu-id="19d9b-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="19d9b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19d9b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="19d9b-114">Remarks</span></span>

<span data-ttu-id="19d9b-115">Essa propriedade é uma das propriedades de endereço do usuário sendo representado pelo usuário recebe mensagens.</span><span class="sxs-lookup"><span data-stu-id="19d9b-115">This property is one of the address properties for the messaging user being represented by the receiving user.</span></span> <span data-ttu-id="19d9b-116">Ele deve ser definido pelo provedor de transporte de entrada, que também é responsável pela verificação do representante ou de autorização.</span><span class="sxs-lookup"><span data-stu-id="19d9b-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="19d9b-117">Se nenhum usuário de mensagens estiver sendo representado, essa propriedade deverá ser definida para a chave de pesquisa contida na propriedade **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="19d9b-117">If no messaging user is being represented, this property should be set to the search key contained in the **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="19d9b-118">Um aplicativo cliente responder a uma mensagem recebida em nome de outro cliente deve copiar essa propriedade de mensagem recebida na propriedade **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) para a resposta.</span><span class="sxs-lookup"><span data-stu-id="19d9b-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="19d9b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="19d9b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19d9b-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="19d9b-120">Protocol specifications</span></span>

<span data-ttu-id="19d9b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19d9b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19d9b-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="19d9b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19d9b-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19d9b-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19d9b-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="19d9b-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="19d9b-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19d9b-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19d9b-126">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="19d9b-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="19d9b-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19d9b-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19d9b-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="19d9b-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="19d9b-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19d9b-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19d9b-130">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="19d9b-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="19d9b-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19d9b-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19d9b-132">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="19d9b-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19d9b-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="19d9b-133">Header files</span></span>

<span data-ttu-id="19d9b-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19d9b-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="19d9b-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="19d9b-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="19d9b-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="19d9b-136">Mapitags.h</span></span>
  
> <span data-ttu-id="19d9b-137">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="19d9b-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19d9b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="19d9b-138">See also</span></span>



[<span data-ttu-id="19d9b-139">Propriedade canônica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="19d9b-139">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)


[<span data-ttu-id="19d9b-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="19d9b-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19d9b-141">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="19d9b-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19d9b-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="19d9b-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19d9b-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="19d9b-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
