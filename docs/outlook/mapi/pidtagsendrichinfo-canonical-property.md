---
title: Propriedade canônica PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342515"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="8e530-103">Propriedade canônica PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="8e530-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="8e530-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e530-105">Contém TRUE se o destinatário pode receber todo o conteúdo da mensagem, incluindo Rich Text Format (RTF) e objetos OLE (vinculação e incorporação de objetos).</span><span class="sxs-lookup"><span data-stu-id="8e530-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e530-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8e530-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e530-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="8e530-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="8e530-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8e530-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e530-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="8e530-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="8e530-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8e530-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e530-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8e530-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8e530-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8e530-112">Area:</span></span>  <br/> |<span data-ttu-id="8e530-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="8e530-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e530-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e530-114">Remarks</span></span>

<span data-ttu-id="8e530-115">É recomendável que a lista de distribuição e os objetos do usuário de mensagens exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8e530-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="8e530-116">Essa propriedade indica se o remetente considera o destinatário como habilitado para MAPI.</span><span class="sxs-lookup"><span data-stu-id="8e530-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="8e530-117">Quando essa propriedade é definida como TRUE, o transporte e o gateway podem transmitir o conteúdo completo da mensagem, incluindo os objetos RTF e OLE.</span><span class="sxs-lookup"><span data-stu-id="8e530-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="8e530-118">O provedor de transporte e o gateway devem usar o formato de encapsulamento de transporte neutro (TNEF) para encapsular quaisquer propriedades que não sejam nativas para todos os sistemas de mensagens envolvidos.</span><span class="sxs-lookup"><span data-stu-id="8e530-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="8e530-119">Quando essa propriedade é definida como FALSE, o provedor de transporte e o gateway estão livres para descartar o conteúdo da mensagem que seus clientes nativos não podem usar.</span><span class="sxs-lookup"><span data-stu-id="8e530-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="8e530-120">Por exemplo, quando os clientes não suportam RTF, o provedor de transporte pode enviar apenas texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="8e530-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="8e530-121">Quando essa propriedade não é definida, o comportamento padrão é determinado pela implementação do provedor de transporte, do agente de transferência de mensagens (MTA) ou do gateway.</span><span class="sxs-lookup"><span data-stu-id="8e530-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="8e530-122">Os provedores de catálogo de endereços não são necessários para dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8e530-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="8e530-123">Por exemplo, um catálogo de endereços e um provedor de transporte rigidamente acoplados podem optar por enviar TNEF, mas nunca usar RTF.</span><span class="sxs-lookup"><span data-stu-id="8e530-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="8e530-124">O cliente não deve assumir que o provedor de transporte e o gateway usarão o TNEF em sua própria iniciativa.</span><span class="sxs-lookup"><span data-stu-id="8e530-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="8e530-125">Alguns provedores de transporte e gateways que dão suporte a TNEF transmitem o valor dessa propriedade, mas outros recusam a construir ou enviarem TNEF se não estiverem definidos como TRUE.</span><span class="sxs-lookup"><span data-stu-id="8e530-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8e530-126">A configuração dessa propriedade e as decisões com base em seu valor, estão em uma base por destinatário.</span><span class="sxs-lookup"><span data-stu-id="8e530-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="8e530-127">Por padrão, o MAPI define o valor como TRUE.</span><span class="sxs-lookup"><span data-stu-id="8e530-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="8e530-128">Um cliente chamando [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) ou um provedor chamando [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) pode definir o bit **MAPI_SEND_NO_RICH_INFO** no parâmetro _PARÂMETROULFLAGS_ , que faz com que o MAPI defina essa propriedade como false.</span><span class="sxs-lookup"><span data-stu-id="8e530-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="8e530-129">Um-offs criados pela interface do usuário usam o valor especificado pelo modelo de criação.</span><span class="sxs-lookup"><span data-stu-id="8e530-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="8e530-130">Em chamadas para o método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) quando o nome não pode ser resolvido, mas pode ser interpretado como um endereço de Internet (SMTP), essa propriedade é definida como false.</span><span class="sxs-lookup"><span data-stu-id="8e530-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="8e530-131">Para ser interpretado como um endereço de Internet, o nome de exibição da entrada não resolvida deve estar no formato X @ Y. Z, como "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="8e530-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e530-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e530-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e530-133">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="8e530-133">Protocol specifications</span></span>

<span data-ttu-id="8e530-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e530-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e530-135">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8e530-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e530-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e530-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e530-137">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="8e530-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="8e530-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e530-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e530-139">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8e530-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8e530-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e530-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e530-141">das convenções de email padrão da Internet para objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8e530-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e530-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e530-142">Header files</span></span>

<span data-ttu-id="8e530-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8e530-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e530-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8e530-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e530-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8e530-145">Mapitags.h</span></span>
  
> <span data-ttu-id="8e530-146">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8e530-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e530-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e530-147">See also</span></span>



[<span data-ttu-id="8e530-148">Propriedade canônica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="8e530-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="8e530-149">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e530-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e530-150">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8e530-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e530-151">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e530-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e530-152">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8e530-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

