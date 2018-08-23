---
title: Propriedade canônica PidTagReceivedRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 490025f22cd643ffededd6d8022907761c7f15d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567094"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="65998-103">Propriedade canônica PidTagReceivedRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="65998-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="65998-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65998-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65998-105">Contém o identificador de entrada para o usuário de mensagens que é representado pelo usuário receptor.</span><span class="sxs-lookup"><span data-stu-id="65998-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65998-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="65998-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65998-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="65998-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="65998-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="65998-108">Identifier:</span></span>  <br/> |<span data-ttu-id="65998-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="65998-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="65998-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="65998-110">Data type:</span></span>  <br/> |<span data-ttu-id="65998-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="65998-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="65998-112">Área:</span><span class="sxs-lookup"><span data-stu-id="65998-112">Area:</span></span>  <br/> |<span data-ttu-id="65998-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="65998-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65998-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="65998-114">Remarks</span></span>

<span data-ttu-id="65998-115">Essa propriedade é uma das propriedades de endereço para o usuário de mensagens que está sendo representado pelo usuário receptor.</span><span class="sxs-lookup"><span data-stu-id="65998-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="65998-116">Ele deve ser definido pelo provedor de transporte de entrada, que também é responsável pela verificação do representante ou de autorização.</span><span class="sxs-lookup"><span data-stu-id="65998-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="65998-117">Se nenhum usuário de mensagens estiver sendo representado, essa propriedade deverá ser definida para o identificador de entrada contido na propriedade **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="65998-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="65998-118">Um aplicativo cliente responder a uma mensagem recebida em nome de outro cliente deve copiar essa propriedade de mensagem recebida na propriedade **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) para a resposta.</span><span class="sxs-lookup"><span data-stu-id="65998-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="65998-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="65998-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65998-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="65998-120">Protocol specifications</span></span>

<span data-ttu-id="65998-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65998-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65998-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="65998-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65998-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65998-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65998-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="65998-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="65998-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65998-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65998-126">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="65998-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="65998-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65998-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65998-128">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="65998-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65998-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="65998-129">Header files</span></span>

<span data-ttu-id="65998-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65998-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="65998-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="65998-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="65998-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="65998-132">Mapitags.h</span></span>
  
> <span data-ttu-id="65998-133">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="65998-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65998-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="65998-134">See also</span></span>



[<span data-ttu-id="65998-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="65998-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65998-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="65998-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65998-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="65998-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65998-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="65998-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

