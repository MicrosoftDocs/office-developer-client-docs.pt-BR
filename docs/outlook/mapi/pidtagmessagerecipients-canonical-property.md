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
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355682"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="52a2a-103">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="52a2a-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="52a2a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52a2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52a2a-105">Contém uma tabela de restrições que podem ser aplicadas a uma tabela de conteúdo para localizar todas as mensagens que contenham subobjetos de destinatário que atendam às restrições.</span><span class="sxs-lookup"><span data-stu-id="52a2a-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52a2a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="52a2a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52a2a-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="52a2a-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="52a2a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="52a2a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52a2a-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="52a2a-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="52a2a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="52a2a-110">Data type:</span></span>  <br/> |<span data-ttu-id="52a2a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="52a2a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="52a2a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="52a2a-112">Area:</span></span>  <br/> |<span data-ttu-id="52a2a-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="52a2a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52a2a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="52a2a-114">Remarks</span></span>

<span data-ttu-id="52a2a-115">Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="52a2a-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="52a2a-116">Como uma propriedade do tipo **PT_OBJECT**, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps.</span><span class="sxs-lookup"><span data-stu-id="52a2a-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="52a2a-117">Seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="52a2a-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="52a2a-118">Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="52a2a-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="52a2a-119">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable.</span><span class="sxs-lookup"><span data-stu-id="52a2a-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="52a2a-120">Essa propriedade pode ser usada para restrição de subobjeto especificando-a na estrutura [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="52a2a-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="52a2a-121">Isso permite que um cliente limite o modo de exibição de um contêiner às mensagens com destinatários que atendem aos critérios fornecidos.</span><span class="sxs-lookup"><span data-stu-id="52a2a-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="52a2a-122">Uma mensagem é qualificada para exibir se pelo menos uma linha na tabela de destinatários, ou seja, um destinatário satisfizer a restrição de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="52a2a-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="52a2a-123">**Observação** O uso de resultados de restrição de subobjeto é o equivalente de uma chamada de [IMAPISession:: OpenEntry](imapisession-openentry.md) em cada mensagem da tabela.</span><span class="sxs-lookup"><span data-stu-id="52a2a-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="52a2a-124">Dependendo do aplicativo cliente e do número de mensagens a serem pesquisadas, isso pode afetar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="52a2a-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="52a2a-125">A propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) e essa propriedade são similares em uso.</span><span class="sxs-lookup"><span data-stu-id="52a2a-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="52a2a-126">Várias propriedades MAPI fornecem acesso a tabelas:</span><span class="sxs-lookup"><span data-stu-id="52a2a-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="52a2a-127">**Property**</span><span class="sxs-lookup"><span data-stu-id="52a2a-127">**Property**</span></span>|<span data-ttu-id="52a2a-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="52a2a-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52a2a-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52a2a-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="52a2a-130">Tabela de conteúdo</span><span class="sxs-lookup"><span data-stu-id="52a2a-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="52a2a-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52a2a-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="52a2a-132">Tabela de hierarquia</span><span class="sxs-lookup"><span data-stu-id="52a2a-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="52a2a-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52a2a-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="52a2a-134">Tabela de conteúdo associado</span><span class="sxs-lookup"><span data-stu-id="52a2a-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="52a2a-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52a2a-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="52a2a-136">Tabela de anexos</span><span class="sxs-lookup"><span data-stu-id="52a2a-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="52a2a-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="52a2a-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="52a2a-138">Tabela de destinatários</span><span class="sxs-lookup"><span data-stu-id="52a2a-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="52a2a-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="52a2a-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52a2a-140">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="52a2a-140">Protocol specifications</span></span>

<span data-ttu-id="52a2a-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52a2a-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52a2a-142">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="52a2a-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="52a2a-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52a2a-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52a2a-144">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="52a2a-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="52a2a-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52a2a-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52a2a-146">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="52a2a-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="52a2a-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52a2a-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52a2a-148">Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="52a2a-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="52a2a-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="52a2a-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="52a2a-150">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="52a2a-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52a2a-151">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52a2a-151">Header files</span></span>

<span data-ttu-id="52a2a-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="52a2a-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="52a2a-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="52a2a-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="52a2a-154">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="52a2a-154">Mapitags.h</span></span>
  
> <span data-ttu-id="52a2a-155">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="52a2a-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52a2a-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="52a2a-156">See also</span></span>



[<span data-ttu-id="52a2a-157">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="52a2a-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52a2a-158">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="52a2a-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52a2a-159">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="52a2a-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52a2a-160">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="52a2a-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

