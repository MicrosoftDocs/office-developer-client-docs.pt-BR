---
title: Propriedade canônica PidTagStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1936cb8e95e3faef8c92d6bf28f5b63b3ff72df5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572701"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="a2dc1-103">Propriedade canônica PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="a2dc1-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="a2dc1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2dc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2dc1-105">Contém uma bitmask dos sinalizadores nessa consulta de aplicativos de cliente para determinar as características de um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2dc1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a2dc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2dc1-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="a2dc1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a2dc1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2dc1-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="a2dc1-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="a2dc1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a2dc1-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2dc1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a2dc1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a2dc1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a2dc1-112">Area:</span></span>  <br/> |<span data-ttu-id="a2dc1-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="a2dc1-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2dc1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2dc1-114">Remarks</span></span>

<span data-ttu-id="a2dc1-115">Essa propriedade revela as capacidades de um armazenamento de mensagens para aplicativos cliente que estiver planejando para enviá-la uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="a2dc1-116">Os sinalizadores podem oferecer suporte a decisões por um cliente ou outro repositório, como se deseja enviar **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou apenas **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a2dc1-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="a2dc1-117">Um cliente nunca deve definir **PR_STORE_SUPPORT_MASK**; uma tentativa de definir este sinalizador retorna MAPI_E_COMPUTED.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="a2dc1-118">Um ou mais dos seguintes sinalizadores podem ser definidas para o bitmask **PR_STORE_SUPPORT_MASK** :</span><span class="sxs-lookup"><span data-stu-id="a2dc1-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="a2dc1-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="a2dc1-120">(131072, 0x00020000) O armazenamento de mensagens oferece suporte a propriedades que contêm caracteres do ANSI (8 bits).</span><span class="sxs-lookup"><span data-stu-id="a2dc1-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="a2dc1-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="a2dc1-122">(32, 0x00000020) O armazenamento de mensagens oferece suporte a anexos (OLE ou não-OLE) às mensagens.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="a2dc1-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="a2dc1-124">(1024, 0x00000400) O armazenamento de mensagens oferece suporte a categorizados modos de exibição das tabelas.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="a2dc1-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="a2dc1-126">(16, 0x00000010) O armazenamento de mensagens oferece suporte a criação de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="a2dc1-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="a2dc1-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="a2dc1-128">(1, 0x00000001) Identificadores de entrada para os objetos no repositório de mensagem são exclusivos, ou seja, nunca reutilizado durante a vida útil do repositório.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="a2dc1-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="a2dc1-130">(65536, 0x00010000) O armazenamento de mensagens oferece suporte a mensagens HTML, armazenadas na propriedade **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a2dc1-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="a2dc1-131">Se seu ambiente de desenvolvimento usa um MAPIDEFS. Arquivo H que não inclui STORE_HTML_OK, use o valor 0x00010000 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="a2dc1-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="a2dc1-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="a2dc1-133">(2097152, 0x00200000) Em um repositório PST encapsulado, indica que, quando uma nova mensagem chega na loja, o repositório executa regras e filtro de spam de processamento na mensagem separadamente.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="a2dc1-134">As repositório chamadas [IMAPISupport::Notify](imapisupport-notify.md), configuração **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e, em seguida, passa os detalhes da nova mensagem para o cliente de escutando.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="a2dc1-135">Subsequentemente, quando o cliente escutando recebe a notificação, ele não processar regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="a2dc1-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="a2dc1-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="a2dc1-137">(524288, 0x00080000) Esse sinalizador é reservado e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="a2dc1-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="a2dc1-139">(8, 0x00000008) O armazenamento de mensagens oferece suporte a modificação das suas mensagens existentes.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="a2dc1-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="a2dc1-141">(512, 0x00000200) O armazenamento de mensagens oferece suporte a vários valores de propriedades, garante a estabilidade da ordem de valor em uma propriedade de valores múltiplos em toda uma gravação de operação e suporta instanciação das propriedades multivaloradas nas tabelas.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="a2dc1-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="a2dc1-143">(256, 0x00000100) O armazenamento de mensagens oferece suporte a notificações.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="a2dc1-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="a2dc1-145">(64, 0x00000040) O armazenamento de mensagens oferece suporte a anexos de OLE.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="a2dc1-146">Os dados OLE podem ser acessados através de uma interface **IStorage** , como disponível por meio da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a2dc1-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="a2dc1-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="a2dc1-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="a2dc1-148">(16384, 0x00004000) As pastas nesse armazenamento são pública (multiusuário), não é particular (possivelmente várias instâncias, mas não multiusuário).</span><span class="sxs-lookup"><span data-stu-id="a2dc1-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="a2dc1-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="a2dc1-150">(8388608, 0x00800000) O manipulador de protocolo MAPI não irá rastrear o repositório e o repositório é responsável para envio quaisquer alterações por meio de notificações por push para o indexador para ter mensagens indexadas.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="a2dc1-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="a2dc1-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="a2dc1-152">(2, 0x00000002) Todas as interfaces para o armazenamento de mensagens têm um nível de acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="a2dc1-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="a2dc1-154">(4096, 0x00001000) O armazenamento de mensagens oferece suporte a restrições.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="a2dc1-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="a2dc1-156">(2048, 0x00000800) O armazenamento de mensagens oferece suporte a mensagens de formato Rich Text (RTF), geralmente compactadas, e o próprio repositório mantém **PR_BODY** e **PR_RTF_COMPRESSED** sincronizados.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="a2dc1-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="a2dc1-158">(268435456, 0x10000000) Indica que as regras devem ser armazenadas nesse repositório PST, mesmo se ele não é o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="a2dc1-159">Quando **STORE_RULES_OK** é usado em conjunto com **NON_EMS_XP_SAVE**, as regras são poderão ser executadas em repositórios de PST quebrado automaticamente não-padrão.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="a2dc1-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="a2dc1-161">(4, 0x00000004) O armazenamento de mensagens oferece suporte a pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="a2dc1-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="a2dc1-163">(8192, 0x00002000) O armazenamento de mensagens oferece suporte a classificação de modos de exibição das tabelas.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="a2dc1-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="a2dc1-165">(128, 0x00000080) O armazenamento de mensagens oferece suporte a marcação de uma mensagem para envio.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="a2dc1-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="a2dc1-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="a2dc1-167">(32768, 0x00008000) O armazenamento de mensagens suporta o armazenamento de mensagens RTF no formato descompactado.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="a2dc1-168">Um fluxo RTF descompactado é identificado pelo valor **dwMagicUncompressedRTF** no cabeçalho stream.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="a2dc1-169">O valor de **dwMagicUncompressedRTF** é definido no RTFLIB. Arquivo H.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="a2dc1-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="a2dc1-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="a2dc1-171">(262144, 0x00040000) Indica que o armazenamento de mensagens oferece suporte a Unicode armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="a2dc1-172">Um cliente pode consultar a presença do sinalizador para decidir se deseja solicitar ou salvar a informação de Unicode para o repositório.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="a2dc1-173">Uma versão RTF de uma mensagem sempre pode ser armazenada, mesmo se o armazenamento de mensagens é sem reconhecimento de RTF.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="a2dc1-174">Se o bit STORE_RTF_OK não estiver definido para um determinado repositório, um cliente de manutenção de versões RTF deve próprio chamar a função [RTFSync](rtfsync.md) para manter as versões de **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas para conteúdo de texto.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="a2dc1-175">RTF sempre será armazenado em **PR_RTF_COMPRESSED**, se ele é realmente compactado ou não.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a2dc1-176">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2dc1-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2dc1-177">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a2dc1-177">Protocol specifications</span></span>

<span data-ttu-id="a2dc1-178">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2dc1-178">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2dc1-179">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2dc1-180">[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2dc1-180">[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2dc1-181">Descreve o formato das mensagens usado para enviar informações relacionadas ao compartilhamento de pastas no cliente.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2dc1-182">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a2dc1-182">Header files</span></span>

<span data-ttu-id="a2dc1-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2dc1-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2dc1-184">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2dc1-185">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a2dc1-185">Mapitags.h</span></span>
  
> <span data-ttu-id="a2dc1-186">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a2dc1-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2dc1-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2dc1-187">See also</span></span>



[<span data-ttu-id="a2dc1-188">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a2dc1-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2dc1-189">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a2dc1-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2dc1-190">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2dc1-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2dc1-191">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a2dc1-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

