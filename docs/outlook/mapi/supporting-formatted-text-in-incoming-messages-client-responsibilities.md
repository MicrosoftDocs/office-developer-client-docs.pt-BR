---
title: Suporte formatado o texto no responsabilidades de cliente de mensagens recebidas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d8fdd9ea4dfbc40d7e800be5e2df666738d2cd23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577454"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="d5152-103">Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="d5152-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="d5152-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5152-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5152-105">Como as mensagens são transferidas entre sistemas de mensagens, o MAPI spooler certifica-se de que a formatação rich text permanecerá sincronizada com o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5152-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="d5152-106">O MAPI spooler chama a função de [RTFSync](rtfsync.md) de dentro de uma versão com quebra da mensagem que ele passa para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="d5152-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="d5152-107">O provedor de transporte salva as alterações feitas à mensagem chamando o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e encaminha para o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="d5152-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="d5152-108">Quando o aplicativo de cliente RTF reconhecimento do destinatário abre a mensagem para exibir o texto, ele deve sincronizar o texto com formatação e abra **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , dependendo de qual propriedade está disponível.</span><span class="sxs-lookup"><span data-stu-id="d5152-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="d5152-109">**Para abrir uma mensagem, os clientes de RTF**</span><span class="sxs-lookup"><span data-stu-id="d5152-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="d5152-110">Chame **RTFSync** para sincronizar o texto da mensagem com a formatação se o armazenamento de mensagens não é sensível ao RTF.</span><span class="sxs-lookup"><span data-stu-id="d5152-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="d5152-111">O sinalizador RTF_SYNC_BODY_CHANGED deve ser passado no parâmetro _ulFlags_ se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver faltando ou defina como FALSE.</span><span class="sxs-lookup"><span data-stu-id="d5152-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="d5152-112">Trabalhando com reconhecimento de RTF armazenamentos de mensagens de clientes não precisam fazer a chamada **RTFSync** porque o armazenamento de mensagens cuida disso.</span><span class="sxs-lookup"><span data-stu-id="d5152-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="d5152-113">Chame [IMAPIProp::SaveChanges](imapiprop-savechanges.md) se o texto da mensagem foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="d5152-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="d5152-114">Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="d5152-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="d5152-115">Se **PR_RTF_COMPRESSED** não estiver disponível, você deve abrir a propriedade **PR_BODY** em vez disso, para exibir o conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5152-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="d5152-116">Chame a função de [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para criar uma versão descompactada dos dados compactados RTF, se disponível.</span><span class="sxs-lookup"><span data-stu-id="d5152-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="d5152-117">Exiba os dados RTF descompactados ou os dados de texto sem formatação para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d5152-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="d5152-118">**RTFSync** retorna um valor Boolean que indica se ou não a mensagem foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="d5152-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="d5152-119">Se esse valor retornar TRUE, chame **SaveChanges** em algum momento para fazer a atualização permanente.</span><span class="sxs-lookup"><span data-stu-id="d5152-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="d5152-120">A chamada não tem a ser feita imediatamente após **RTFSync** retorna.</span><span class="sxs-lookup"><span data-stu-id="d5152-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d5152-121">Como componentes tantos manipular o texto formatado antes de você recebê-la, há a possibilidade dos danos.</span><span class="sxs-lookup"><span data-stu-id="d5152-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="d5152-122">Essa corrupção poderia provenientes de um aplicativo de terceiros, o provedor de armazenamento de mensagem, um gateway ou um erro de transmissão.</span><span class="sxs-lookup"><span data-stu-id="d5152-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

