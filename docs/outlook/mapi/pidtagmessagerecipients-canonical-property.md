---
title: Propriedade canônica PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 980b1b81a0afbfe05fee915ddd730aad31811132
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769484"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="95351-103">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="95351-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="95351-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95351-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95351-105">Contém uma tabela das restrições que podem ser aplicadas a uma tabela de conteúdo para localizar todas as mensagens que contêm o destinatários subobjetos que atendam as restrições.</span><span class="sxs-lookup"><span data-stu-id="95351-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95351-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="95351-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95351-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="95351-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="95351-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="95351-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95351-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="95351-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="95351-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="95351-110">Data type:</span></span>  <br/> |<span data-ttu-id="95351-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="95351-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="95351-112">Área:</span><span class="sxs-lookup"><span data-stu-id="95351-112">Area:</span></span>  <br/> |<span data-ttu-id="95351-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="95351-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95351-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="95351-114">Remarks</span></span>

<span data-ttu-id="95351-115">Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="95351-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="95351-116">Como uma propriedade do tipo **PT_OBJECT**, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="95351-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="95351-117">Seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="95351-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="95351-118">Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas opcionalmente relatá-la ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="95351-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="95351-119">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="95351-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="95351-120">Essa propriedade pode ser usada para restrição subobjeto especificando-o na estrutura [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="95351-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="95351-121">Isso permite que um cliente limitar o modo de exibição de um contêiner para mensagens com destinatários da reunião determinado critério.</span><span class="sxs-lookup"><span data-stu-id="95351-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="95351-122">Uma mensagem qualifica para exibição se pelo menos uma linha em sua tabela de destinatário, ou seja, um destinatário atenda a restrição subobjeto.</span><span class="sxs-lookup"><span data-stu-id="95351-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="95351-123">**Observação** Usando os resultados da restrição subobjeto é o equivalente a um [IMAPISession::OpenEntry](imapisession-openentry.md) chama em todas as mensagens na tabela.</span><span class="sxs-lookup"><span data-stu-id="95351-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="95351-124">Dependendo do aplicativo cliente e o número de mensagens a ser pesquisado, ele pode afetar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="95351-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="95351-125">A propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) e essa propriedade são semelhantes em uso.</span><span class="sxs-lookup"><span data-stu-id="95351-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="95351-126">Várias propriedades MAPI fornecem acesso às tabelas:</span><span class="sxs-lookup"><span data-stu-id="95351-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="95351-127">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="95351-127">**Property**</span></span>|<span data-ttu-id="95351-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="95351-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95351-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95351-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95351-130">Tabela de conteúdo</span><span class="sxs-lookup"><span data-stu-id="95351-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="95351-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95351-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95351-132">Tabela de hierarquia</span><span class="sxs-lookup"><span data-stu-id="95351-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="95351-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95351-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95351-134">Tabela de conteúdo associado</span><span class="sxs-lookup"><span data-stu-id="95351-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="95351-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95351-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95351-136">Tabela de anexos</span><span class="sxs-lookup"><span data-stu-id="95351-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="95351-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="95351-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="95351-138">Tabela de destinatários</span><span class="sxs-lookup"><span data-stu-id="95351-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="95351-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="95351-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95351-140">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="95351-140">Protocol specifications</span></span>

<span data-ttu-id="95351-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95351-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95351-142">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="95351-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95351-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95351-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95351-144">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="95351-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="95351-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95351-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95351-146">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="95351-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="95351-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95351-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95351-148">Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="95351-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="95351-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95351-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95351-150">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="95351-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95351-151">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="95351-151">Header files</span></span>

<span data-ttu-id="95351-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95351-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="95351-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="95351-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="95351-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95351-154">Mapitags.h</span></span>
  
> <span data-ttu-id="95351-155">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="95351-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95351-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="95351-156">See also</span></span>



[<span data-ttu-id="95351-157">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="95351-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95351-158">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="95351-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95351-159">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="95351-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95351-160">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="95351-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

