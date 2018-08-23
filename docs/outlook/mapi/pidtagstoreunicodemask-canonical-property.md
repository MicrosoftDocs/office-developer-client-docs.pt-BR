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
ms.openlocfilehash: 4bfbaada3ced58a689ca4d4745e6e4c798755d4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574304"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="f30bf-103">Propriedade canônica PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="f30bf-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="f30bf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f30bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f30bf-105">Contém uma bitmask dos sinalizadores que aplicativos cliente devem consultar para determinar as características de um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f30bf-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f30bf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f30bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f30bf-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="f30bf-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="f30bf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f30bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f30bf-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="f30bf-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="f30bf-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f30bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="f30bf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f30bf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f30bf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f30bf-112">Area:</span></span>  <br/> |<span data-ttu-id="f30bf-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="f30bf-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f30bf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f30bf-114">Remarks</span></span>

<span data-ttu-id="f30bf-115">Essa propriedade revela as capacidades de um armazenamento de mensagens para aplicativos cliente do planejamento para enviá-la uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f30bf-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="f30bf-116">Os sinalizadores podem facilitar decisões por um cliente ou outro repositório, como se deseja enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f30bf-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="f30bf-117">Um cliente nunca deve definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f30bf-117">A client should never set this property.</span></span> <span data-ttu-id="f30bf-118">Uma tentativa retorna **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="f30bf-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="f30bf-119">Um ou mais dos seguintes sinalizadores podem ser definido para essa propriedade:</span><span class="sxs-lookup"><span data-stu-id="f30bf-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="f30bf-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="f30bf-121">(131072, 0x00020000) O armazenamento de mensagens oferece suporte a propriedades que contêm caracteres (8 bits), American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f30bf-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="f30bf-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="f30bf-123">(32, 0x00000020) O armazenamento de mensagens oferece suporte a vinculação e incorporação de objetos (OLE) ou não-OLE anexos de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f30bf-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="f30bf-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="f30bf-125">(1024, 0x00000400) O armazenamento de mensagens oferece suporte a categorizados modos de exibição das tabelas.</span><span class="sxs-lookup"><span data-stu-id="f30bf-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="f30bf-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="f30bf-127">(16, 0x00000010) O armazenamento de mensagens oferece suporte a criação de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="f30bf-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="f30bf-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="f30bf-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="f30bf-129">(1, 0x00000001) Identificadores de entrada para os objetos no repositório de mensagem são exclusivos, ou seja, nunca reutilizado durante a vida útil do repositório.</span><span class="sxs-lookup"><span data-stu-id="f30bf-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="f30bf-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="f30bf-131">(65536, 0x00010000) O armazenamento de mensagens oferece suporte a mensagens HTML, armazenadas na propriedade **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f30bf-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="f30bf-132">Observe que **STORE_HTML_OK** não está definido em versões do MAPIDEFS. H que estão incluídos no Microsoft Exchange 2000 Server e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f30bf-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="f30bf-133">Se seu ambiente de desenvolvimento usa um MAPIDEFS. Arquivo de H que não incluem **STORE_HTML_OK**, use o valor da "0x00010000".</span><span class="sxs-lookup"><span data-stu-id="f30bf-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="f30bf-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="f30bf-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="f30bf-135">(2097152, 0x00200000) Em um repositório PST encapsulado, indica que quando uma nova mensagem chega na loja, o repositório faz regras e spam filtrar processamento na mensagem separadamente.</span><span class="sxs-lookup"><span data-stu-id="f30bf-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="f30bf-136">As repositório chamadas [IMAPISupport::Notify](imapisupport-notify.md), configuração **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e, em seguida, passa os detalhes da nova mensagem para o cliente de escutando.</span><span class="sxs-lookup"><span data-stu-id="f30bf-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="f30bf-137">Subsequentemente, quando o cliente escutando recebe a notificação, ele não processar regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="f30bf-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="f30bf-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="f30bf-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="f30bf-139">(524288, 0x00080000) Esse sinalizador é reservado e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="f30bf-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="f30bf-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="f30bf-141">(8, 0x00000008) O armazenamento de mensagens oferece suporte a modificação das suas mensagens existentes.</span><span class="sxs-lookup"><span data-stu-id="f30bf-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="f30bf-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="f30bf-143">(512, 0x00000200) O armazenamento de mensagens oferece suporte a vários valores de propriedades, garante a estabilidade da ordem de valor em uma propriedade de valores múltiplos em toda uma gravação de operação e suporta instanciação das propriedades multivaloradas nas tabelas.</span><span class="sxs-lookup"><span data-stu-id="f30bf-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="f30bf-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="f30bf-145">(256, 0x00000100) O armazenamento de mensagens oferece suporte a notificações.</span><span class="sxs-lookup"><span data-stu-id="f30bf-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="f30bf-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="f30bf-147">(64, 0x00000040) O armazenamento de mensagens oferece suporte a anexos de OLE.</span><span class="sxs-lookup"><span data-stu-id="f30bf-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="f30bf-148">Os dados OLE são acessíveis através de uma interface **IStorage** , tais como isto disponíveis por meio da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f30bf-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="f30bf-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="f30bf-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="f30bf-150">(16384, 0x00004000) As pastas nesse armazenamento são pública (multiusuário), não é particular (possivelmente várias instâncias, mas não multiusuário).</span><span class="sxs-lookup"><span data-stu-id="f30bf-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="f30bf-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="f30bf-152">(8388608, 0x00800000) O manipulador de protocolo MAPI não irá rastrear o repositório e o repositório é responsável por push quaisquer alterações por meio de notificações para o indexador para ter mensagens indexadas.</span><span class="sxs-lookup"><span data-stu-id="f30bf-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="f30bf-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="f30bf-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="f30bf-154">(2, 0x00000002) Todas as interfaces para o armazenamento de mensagens têm um nível de acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f30bf-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="f30bf-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="f30bf-156">(4096, 0x00001000) O armazenamento de mensagens oferece suporte a restrições.</span><span class="sxs-lookup"><span data-stu-id="f30bf-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="f30bf-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="f30bf-158">(2048, 0x00000800) O armazenamento de mensagens oferece suporte a mensagens de formato Rich Text (RTF), geralmente compactadas, e o próprio repositório mantém **PR_BODY** e **PR_RTF_COMPRESSED** sincronizados.</span><span class="sxs-lookup"><span data-stu-id="f30bf-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="f30bf-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="f30bf-160">(4, 0x00000004) O armazenamento de mensagens oferece suporte a pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f30bf-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="f30bf-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="f30bf-162">(8192, 0x00002000) O armazenamento de mensagens oferece suporte a classificação de modos de exibição das tabelas.</span><span class="sxs-lookup"><span data-stu-id="f30bf-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="f30bf-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="f30bf-164">(128, 0x00000080) O armazenamento de mensagens oferece suporte a marcação de uma mensagem para envio.</span><span class="sxs-lookup"><span data-stu-id="f30bf-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="f30bf-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="f30bf-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="f30bf-166">(32768, 0x00008000) O armazenamento de mensagens suporta o armazenamento de mensagens de texto (RTF) do formulário revisable descompactado.</span><span class="sxs-lookup"><span data-stu-id="f30bf-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="f30bf-167">Um fluxo RTF descompactado é identificado pelo valor **dwMagicUncompressedRTF** no cabeçalho stream.</span><span class="sxs-lookup"><span data-stu-id="f30bf-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="f30bf-168">O valor de **dwMagicUncompressedRTF** é definido no RTFLIB. Arquivo H.</span><span class="sxs-lookup"><span data-stu-id="f30bf-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="f30bf-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="f30bf-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="f30bf-170">(262144, 0x00040000) O armazenamento de mensagens oferece suporte a propriedades que contém caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f30bf-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="f30bf-171">Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o armazenamento de mensagens é sem reconhecimento de RTF.</span><span class="sxs-lookup"><span data-stu-id="f30bf-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="f30bf-172">Se o bit STORE_RTF_OK não estiver definido para um determinado repositório, um cliente de manutenção de versões RTF deve próprio chamar a função [RTFSync](rtfsync.md) para manter as versões de **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para conteúdo de texto.</span><span class="sxs-lookup"><span data-stu-id="f30bf-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="f30bf-173">RTF sempre será armazenado em **PR_RTF_COMPRESSED**, se ele é realmente compactado ou não.</span><span class="sxs-lookup"><span data-stu-id="f30bf-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f30bf-174">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f30bf-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f30bf-175">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f30bf-175">Header files</span></span>

<span data-ttu-id="f30bf-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f30bf-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="f30bf-177">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f30bf-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="f30bf-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f30bf-178">Mapitags.h</span></span>
  
> <span data-ttu-id="f30bf-179">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f30bf-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f30bf-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="f30bf-180">See also</span></span>



[<span data-ttu-id="f30bf-181">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f30bf-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f30bf-182">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f30bf-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f30bf-183">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f30bf-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f30bf-184">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f30bf-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

