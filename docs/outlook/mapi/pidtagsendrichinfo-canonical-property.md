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
ms.openlocfilehash: a85851663c22b33ea94099ac0ab14f81c424259b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770003"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="9b27a-103">Propriedade canônica PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="9b27a-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="9b27a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b27a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b27a-105">Contém TRUE se o destinatário poderá receber todo o conteúdo de mensagem, incluindo formato Rich Text (RTF) e objetos de vinculação e incorporação de objetos (OLE).</span><span class="sxs-lookup"><span data-stu-id="9b27a-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b27a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9b27a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b27a-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="9b27a-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="9b27a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b27a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b27a-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="9b27a-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="9b27a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9b27a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b27a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9b27a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9b27a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9b27a-112">Area:</span></span>  <br/> |<span data-ttu-id="9b27a-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="9b27a-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b27a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b27a-114">Remarks</span></span>

<span data-ttu-id="9b27a-115">É recomendável que a lista de distribuição e objetos de usuário de mensagens exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9b27a-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="9b27a-116">Esta propriedade indica se o remetente considera o destinatário a ser habilitado a MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b27a-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="9b27a-117">Quando essa propriedade é definida como TRUE, o transporte e o gateway podem transmitir todo o conteúdo da mensagem, incluindo os objetos OLE e RTF.</span><span class="sxs-lookup"><span data-stu-id="9b27a-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="9b27a-118">O provedor de transporte e o gateway devem usar o TNEF Transport Neutral Encapsulation Format () para encapsular todas as propriedades que não são nativas todos os sistemas mensagens envolvidos.</span><span class="sxs-lookup"><span data-stu-id="9b27a-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="9b27a-119">Quando essa propriedade é definida como FALSE, o provedor de transporte e o gateway são livres para descartar o conteúdo da mensagem que não é possível usar a seus clientes nativos.</span><span class="sxs-lookup"><span data-stu-id="9b27a-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="9b27a-120">Por exemplo, quando os clientes não suportam RTF, o provedor de transporte que pode enviar apenas texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="9b27a-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="9b27a-121">Quando essa propriedade não estiver definida, o comportamento padrão é determinado pela implementação do provedor de transporte, o agente de transferência de mensagem (MTA) ou gateway.</span><span class="sxs-lookup"><span data-stu-id="9b27a-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="9b27a-122">Provedores de catálogo de endereços não são necessárias para dar suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9b27a-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="9b27a-123">Por exemplo, um provedor de transporte e o catálogo de endereços ligação estreita pode optar por enviar TNEF, mas nunca usar o formato RTF.</span><span class="sxs-lookup"><span data-stu-id="9b27a-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="9b27a-124">O cliente não deve supor que o provedor de transporte e o gateway usará o TNEF em sua própria iniciativa.</span><span class="sxs-lookup"><span data-stu-id="9b27a-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="9b27a-125">Alguns provedores de transporte e gateways que oferecem suporte TNEF transmitem sem relação com o valor dessa propriedade, mas outros recusar construir ou enviar o TNEF se ele não estiver definido como TRUE.</span><span class="sxs-lookup"><span data-stu-id="9b27a-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9b27a-126">A configuração desta propriedade, e as decisões com base em seu valor, estão em uma base por destinatário.</span><span class="sxs-lookup"><span data-stu-id="9b27a-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="9b27a-127">Por padrão, o MAPI define o valor como TRUE.</span><span class="sxs-lookup"><span data-stu-id="9b27a-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="9b27a-128">Um cliente chamar [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) ou um provedor chamar [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) pode definir o bit **MAPI_SEND_NO_RICH_INFO** no parâmetro _ulFlags_ , que faz com que o MAPI definir essa propriedade como FALSE.</span><span class="sxs-lookup"><span data-stu-id="9b27a-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="9b27a-129">Algo isolado criados pela interface do usuário use o valor especificado pelo modelo de criação.</span><span class="sxs-lookup"><span data-stu-id="9b27a-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="9b27a-130">Em chamadas para o método [IAddrBook::ResolveName](iaddrbook-resolvename.md) quando o nome não pode ser resolvido, mas pode ser interpretado como um endereço de Internet (SMTP), essa propriedade é definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="9b27a-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="9b27a-131">Para ser interpretado como um endereço de Internet, o nome para exibição da entrada de não-resolvida deve estar no formato X@Y. Z, como "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="9b27a-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9b27a-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b27a-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b27a-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9b27a-133">Protocol specifications</span></span>

<span data-ttu-id="9b27a-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b27a-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b27a-135">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9b27a-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b27a-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b27a-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b27a-137">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="9b27a-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="9b27a-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b27a-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b27a-139">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9b27a-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="9b27a-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b27a-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b27a-141">os objetos de convenções de email padrão da Internet para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="9b27a-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b27a-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9b27a-142">Header files</span></span>

<span data-ttu-id="9b27a-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b27a-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b27a-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b27a-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b27a-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b27a-145">Mapitags.h</span></span>
  
> <span data-ttu-id="9b27a-146">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="9b27a-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b27a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b27a-147">See also</span></span>



[<span data-ttu-id="9b27a-148">Propriedade canônica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="9b27a-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="9b27a-149">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b27a-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b27a-150">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9b27a-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b27a-151">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b27a-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b27a-152">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9b27a-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

