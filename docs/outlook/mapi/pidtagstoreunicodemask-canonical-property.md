---
title: Propriedade canônica PidTagStoreUnicodeMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437935"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="494d9-103">Propriedade canônica PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="494d9-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="494d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="494d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="494d9-105">Contém uma máscara de bits de sinalizadores que os aplicativos cliente devem consultar para determinar as características de um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="494d9-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="494d9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="494d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="494d9-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="494d9-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="494d9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="494d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="494d9-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="494d9-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="494d9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="494d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="494d9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="494d9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="494d9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="494d9-112">Area:</span></span>  <br/> |<span data-ttu-id="494d9-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="494d9-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="494d9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="494d9-114">Remarks</span></span>

<span data-ttu-id="494d9-115">Essa propriedade divulga os recursos de um armazenamento de mensagens para aplicativos cliente que planejam enviar uma mensagem a ele.</span><span class="sxs-lookup"><span data-stu-id="494d9-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="494d9-116">Os sinalizadores podem facilitar as decisões por um cliente ou outro armazenamento, como se você deve enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="494d9-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="494d9-117">Um cliente nunca deve definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="494d9-117">A client should never set this property.</span></span> <span data-ttu-id="494d9-118">Uma tentativa retorna **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="494d9-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="494d9-119">Um ou mais dos sinalizadores a seguir podem ser definidos para essa propriedade:</span><span class="sxs-lookup"><span data-stu-id="494d9-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="494d9-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="494d9-121">(131072, 0x00020000) O armazenamento de mensagens oferece suporte a propriedades que contêm caracteres anSI (American National Standards Institute) (8 bits).</span><span class="sxs-lookup"><span data-stu-id="494d9-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="494d9-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="494d9-123">(32, 0x00000020) O armazenamento de mensagens dá suporte a OLE (Vinculação e Incorporação de Objetos) ou anexos não OLE a mensagens.</span><span class="sxs-lookup"><span data-stu-id="494d9-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="494d9-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="494d9-125">(1024, 0x00000400) O armazenamento de mensagens dá suporte a exibições categorizadas de tabelas.</span><span class="sxs-lookup"><span data-stu-id="494d9-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="494d9-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="494d9-127">(16, 0x00000010) O armazenamento de mensagens oferece suporte à criação de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="494d9-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="494d9-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="494d9-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="494d9-129">(1, 0x00000001) Os identificadores de entrada para os objetos no armazenamento de mensagens são exclusivos, ou seja, nunca reutilizáveis durante a vida útil do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="494d9-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="494d9-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="494d9-131">(65536, 0x00010000) O armazenamento de mensagens dá suporte a mensagens HTML, armazenadas **na PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="494d9-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="494d9-132">Observe que **STORE_HTML_OK** não está definido em versões de MAPIDEFS. H que estão incluídos no Microsoft Exchange 2000 Server e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="494d9-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="494d9-133">Se seu ambiente de desenvolvimento usa um MAPIDEFS. Arquivo H que não **inclui** STORE_HTML_OK , use o valor "0x00010000".</span><span class="sxs-lookup"><span data-stu-id="494d9-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="494d9-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="494d9-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="494d9-135">(2097152, 0x00200000) Em um armazenamento PST empacotado, indica que, quando uma nova mensagem chega ao armazenamento, o armazenamento faz o processamento de regras e filtros de spam na mensagem separadamente.</span><span class="sxs-lookup"><span data-stu-id="494d9-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="494d9-136">O armazenamento chama [IMAPISupport::Notify](imapisupport-notify.md), definindo **fnevNewMail** na estrutura [NOTIFICATION](notification.md) que é passada como um parâmetro e passa os detalhes da nova mensagem para o cliente de escuta.</span><span class="sxs-lookup"><span data-stu-id="494d9-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="494d9-137">Posteriormente, quando o cliente de escutará recebe a notificação, ele não processará regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="494d9-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="494d9-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="494d9-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="494d9-139">(524288, 0x00080000) Esse sinalizador é reservado e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="494d9-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="494d9-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="494d9-141">(8, 0x00000008) O armazenamento de mensagens dá suporte à modificação de suas mensagens existentes.</span><span class="sxs-lookup"><span data-stu-id="494d9-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="494d9-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="494d9-143">(512, 0x00000200) O armazenamento de mensagens oferece suporte a propriedades de múltiplos valores, garante a estabilidade da ordem de valor em uma propriedade de múltiplos valores ao longo de uma operação de salvar e oferece suporte à instaciação de propriedades de múltiplos valores em tabelas.</span><span class="sxs-lookup"><span data-stu-id="494d9-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="494d9-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="494d9-145">(256, 0x00000100) O armazenamento de mensagens oferece suporte a notificações.</span><span class="sxs-lookup"><span data-stu-id="494d9-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="494d9-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="494d9-147">(64, 0x00000040) O armazenamento de mensagens dá suporte a anexos OLE.</span><span class="sxs-lookup"><span data-stu-id="494d9-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="494d9-148">Os dados OLE podem ser acessados por meio de uma interface **IStorage,** como os disponíveis por meio da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="494d9-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="494d9-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="494d9-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="494d9-150">(16384, 0x00004000) As pastas nesse armazenamento são públicas (multiusuárias), não privadas (possivelmente com várias instâncias, mas não com vários usuários).</span><span class="sxs-lookup"><span data-stu-id="494d9-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="494d9-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="494d9-152">(8388608, 0x00800000) O Manipulador de Protocolo MAPI não rastreará o armazenamento, e o armazenamento é responsável por enviar quaisquer alterações por meio de notificações ao indexador para que as mensagens tenham sido indexadas.</span><span class="sxs-lookup"><span data-stu-id="494d9-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="494d9-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="494d9-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="494d9-154">(2, 0x00000002) Todas as interfaces para o armazenamento de mensagens têm um nível de acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="494d9-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="494d9-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="494d9-156">(4096, 0x00001000) O armazenamento de mensagens oferece suporte a restrições.</span><span class="sxs-lookup"><span data-stu-id="494d9-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="494d9-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="494d9-158">(2048, 0x00000800) O armazenamento de mensagens dá suporte a mensagens RTF (Rich Text Format), geralmente compactadas, e o próprio armazenamento mantém PR_BODY **e** **PR_RTF_COMPRESSED** sincronizados.</span><span class="sxs-lookup"><span data-stu-id="494d9-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="494d9-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="494d9-160">(4, 0x00000004) O armazenamento de mensagens oferece suporte a pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="494d9-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="494d9-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="494d9-162">(8192, 0x00002000) O armazenamento de mensagens oferece suporte à classificação de exibições de tabelas.</span><span class="sxs-lookup"><span data-stu-id="494d9-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="494d9-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="494d9-164">(128, 0x00000080) O armazenamento de mensagens dá suporte à marcação de uma mensagem para envio.</span><span class="sxs-lookup"><span data-stu-id="494d9-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="494d9-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="494d9-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="494d9-166">(32768, 0x00008000) O armazenamento de mensagens oferece suporte ao armazenamento de mensagens de texto de formulário revisível (RTF) em formato não compactado.</span><span class="sxs-lookup"><span data-stu-id="494d9-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="494d9-167">Um fluxo RTF não compactado é identificado pelo valor **dwMagicUncompressedRTF** no header de fluxo.</span><span class="sxs-lookup"><span data-stu-id="494d9-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="494d9-168">O **valor dwMagicUncompressedRTF** é definido no RTFLIB. Arquivo H.</span><span class="sxs-lookup"><span data-stu-id="494d9-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="494d9-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="494d9-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="494d9-170">(262144, 0x00040000) O armazenamento de mensagens dá suporte a propriedades que contêm caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="494d9-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="494d9-171">Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o armazenamento de mensagens não reconhece RTF.</span><span class="sxs-lookup"><span data-stu-id="494d9-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="494d9-172">Se o bit STORE_RTF_OK não estiver definido para um determinado armazenamento, um cliente que mantém versões RTF deverá chamar a função [RTFSync](rtfsync.md) para manter as versões **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para conteúdo de texto.</span><span class="sxs-lookup"><span data-stu-id="494d9-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="494d9-173">O RTF é sempre armazenado **PR_RTF_COMPRESSED**, seja realmente compactado ou não.</span><span class="sxs-lookup"><span data-stu-id="494d9-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="494d9-174">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="494d9-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="494d9-175">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="494d9-175">Header files</span></span>

<span data-ttu-id="494d9-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="494d9-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="494d9-177">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="494d9-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="494d9-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="494d9-178">Mapitags.h</span></span>
  
> <span data-ttu-id="494d9-179">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="494d9-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="494d9-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="494d9-180">See also</span></span>



[<span data-ttu-id="494d9-181">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="494d9-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="494d9-182">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="494d9-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="494d9-183">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="494d9-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="494d9-184">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="494d9-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

