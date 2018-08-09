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
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770092"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="868b7-103">Propriedade canônica PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="868b7-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="868b7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="868b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="868b7-105">Contém uma bitmask dos sinalizadores que aplicativos cliente devem consultar para determinar as características de um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="868b7-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="868b7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="868b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="868b7-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="868b7-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="868b7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="868b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="868b7-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="868b7-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="868b7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="868b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="868b7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="868b7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="868b7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="868b7-112">Area:</span></span>  <br/> |<span data-ttu-id="868b7-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="868b7-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="868b7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="868b7-114">Remarks</span></span>

<span data-ttu-id="868b7-115">Essa propriedade revela as capacidades de um armazenamento de mensagens para aplicativos cliente do planejamento para enviá-la uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="868b7-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="868b7-116">Os sinalizadores podem facilitar decisões por um cliente ou outro repositório, como se deseja enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="868b7-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="868b7-117">Um cliente nunca deve definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="868b7-117">A client should never set this property.</span></span> <span data-ttu-id="868b7-118">Uma tentativa retorna **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="868b7-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="868b7-119">Um ou mais dos seguintes sinalizadores podem ser definido para essa propriedade:</span><span class="sxs-lookup"><span data-stu-id="868b7-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="868b7-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="868b7-121">(131072, 0x00020000) O armazenamento de mensagens oferece suporte a propriedades que contêm caracteres (8 bits), American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="868b7-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="868b7-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="868b7-123">(32, 0x00000020) O armazenamento de mensagens oferece suporte a vinculação e incorporação de objetos (OLE) ou não-OLE anexos de mensagens.</span><span class="sxs-lookup"><span data-stu-id="868b7-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="868b7-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="868b7-125">(1024, 0x00000400) O armazenamento de mensagens oferece suporte a categorizados modos de exibição das tabelas.</span><span class="sxs-lookup"><span data-stu-id="868b7-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="868b7-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="868b7-127">(16, 0x00000010) O armazenamento de mensagens oferece suporte a criação de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="868b7-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="868b7-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="868b7-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="868b7-129">(1, 0x00000001) Identificadores de entrada para os objetos no repositório de mensagem são exclusivos, ou seja, nunca reutilizado durante a vida útil do repositório.</span><span class="sxs-lookup"><span data-stu-id="868b7-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="868b7-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="868b7-131">(65536, 0x00010000) O armazenamento de mensagens oferece suporte a mensagens HTML, armazenadas na propriedade **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="868b7-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="868b7-132">Observe que **STORE_HTML_OK** não está definido em versões do MAPIDEFS. H que estão incluídos no Microsoft Exchange 2000 Server e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="868b7-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="868b7-133">Se seu ambiente de desenvolvimento usa um MAPIDEFS. Arquivo de H que não incluem **STORE_HTML_OK**, use o valor da "0x00010000".</span><span class="sxs-lookup"><span data-stu-id="868b7-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="868b7-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="868b7-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="868b7-135">(2097152, 0x00200000) Em um repositório PST encapsulado, indica que quando uma nova mensagem chega na loja, o repositório faz regras e spam filtrar processamento na mensagem separadamente.</span><span class="sxs-lookup"><span data-stu-id="868b7-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="868b7-136">As repositório chamadas [IMAPISupport::Notify](imapisupport-notify.md), configuração **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e, em seguida, passa os detalhes da nova mensagem para o cliente de escutando.</span><span class="sxs-lookup"><span data-stu-id="868b7-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="868b7-137">Subsequentemente, quando o cliente escutando recebe a notificação, ele não processar regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="868b7-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="868b7-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="868b7-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="868b7-139">(524288, 0x00080000) Esse sinalizador é reservado e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="868b7-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="868b7-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="868b7-141">(8, 0x00000008) O armazenamento de mensagens oferece suporte a modificação das suas mensagens existentes.</span><span class="sxs-lookup"><span data-stu-id="868b7-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="868b7-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="868b7-143">(512, 0x00000200) O armazenamento de mensagens oferece suporte a vários valores de propriedades, garante a estabilidade da ordem de valor em uma propriedade de valores múltiplos em toda uma gravação de operação e suporta instanciação das propriedades multivaloradas nas tabelas.</span><span class="sxs-lookup"><span data-stu-id="868b7-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="868b7-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="868b7-145">(256, 0x00000100) O armazenamento de mensagens oferece suporte a notificações.</span><span class="sxs-lookup"><span data-stu-id="868b7-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="868b7-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="868b7-147">(64, 0x00000040) O armazenamento de mensagens oferece suporte a anexos de OLE.</span><span class="sxs-lookup"><span data-stu-id="868b7-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="868b7-148">Os dados OLE são acessíveis através de uma interface **IStorage** , tais como isto disponíveis por meio da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="868b7-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="868b7-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="868b7-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="868b7-150">(16384, 0x00004000) As pastas nesse armazenamento são pública (multiusuário), não é particular (possivelmente várias instâncias, mas não multiusuário).</span><span class="sxs-lookup"><span data-stu-id="868b7-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="868b7-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="868b7-152">(8388608, 0x00800000) O manipulador de protocolo MAPI não irá rastrear o repositório e o repositório é responsável por push quaisquer alterações por meio de notificações para o indexador para ter mensagens indexadas.</span><span class="sxs-lookup"><span data-stu-id="868b7-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="868b7-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="868b7-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="868b7-154">(2, 0x00000002) Todas as interfaces para o armazenamento de mensagens têm um nível de acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="868b7-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="868b7-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="868b7-156">(4096, 0x00001000) O armazenamento de mensagens oferece suporte a restrições.</span><span class="sxs-lookup"><span data-stu-id="868b7-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="868b7-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="868b7-158">(2048, 0x00000800) O armazenamento de mensagens oferece suporte a mensagens de formato Rich Text (RTF), geralmente compactadas, e o próprio repositório mantém **PR_BODY** e **PR_RTF_COMPRESSED** sincronizados.</span><span class="sxs-lookup"><span data-stu-id="868b7-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="868b7-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="868b7-160">(4, 0x00000004) O armazenamento de mensagens oferece suporte a pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="868b7-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="868b7-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="868b7-162">(8192, 0x00002000) O armazenamento de mensagens oferece suporte a classificação de modos de exibição das tabelas.</span><span class="sxs-lookup"><span data-stu-id="868b7-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="868b7-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="868b7-164">(128, 0x00000080) O armazenamento de mensagens oferece suporte a marcação de uma mensagem para envio.</span><span class="sxs-lookup"><span data-stu-id="868b7-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="868b7-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="868b7-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="868b7-166">(32768, 0x00008000) O armazenamento de mensagens suporta o armazenamento de mensagens de texto (RTF) do formulário revisable descompactado.</span><span class="sxs-lookup"><span data-stu-id="868b7-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="868b7-167">Um fluxo RTF descompactado é identificado pelo valor **dwMagicUncompressedRTF** no cabeçalho stream.</span><span class="sxs-lookup"><span data-stu-id="868b7-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="868b7-168">O valor de **dwMagicUncompressedRTF** é definido no RTFLIB. Arquivo H.</span><span class="sxs-lookup"><span data-stu-id="868b7-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="868b7-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="868b7-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="868b7-170">(262144, 0x00040000) O armazenamento de mensagens oferece suporte a propriedades que contém caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="868b7-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="868b7-171">Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o armazenamento de mensagens é sem reconhecimento de RTF.</span><span class="sxs-lookup"><span data-stu-id="868b7-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="868b7-172">Se o bit STORE_RTF_OK não estiver definido para um determinado repositório, um cliente de manutenção de versões RTF deve próprio chamar a função [RTFSync](rtfsync.md) para manter as versões de **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para conteúdo de texto.</span><span class="sxs-lookup"><span data-stu-id="868b7-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="868b7-173">RTF sempre será armazenado em **PR_RTF_COMPRESSED**, se ele é realmente compactado ou não.</span><span class="sxs-lookup"><span data-stu-id="868b7-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="868b7-174">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="868b7-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="868b7-175">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="868b7-175">Header files</span></span>

<span data-ttu-id="868b7-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="868b7-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="868b7-177">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="868b7-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="868b7-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="868b7-178">Mapitags.h</span></span>
  
> <span data-ttu-id="868b7-179">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="868b7-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="868b7-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="868b7-180">See also</span></span>



[<span data-ttu-id="868b7-181">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="868b7-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="868b7-182">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="868b7-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="868b7-183">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="868b7-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="868b7-184">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="868b7-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

