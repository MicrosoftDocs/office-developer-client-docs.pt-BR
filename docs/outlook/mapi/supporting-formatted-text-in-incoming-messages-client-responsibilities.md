---
title: Suporte a texto formatado em responsabilidades do cliente de mensagens de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434498"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="87c1e-103">Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="87c1e-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="87c1e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87c1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87c1e-105">À medida que as mensagens são transferidas entre sistemas de mensagens, o spooler MAPI garante que a formatação rich text permaneça sincronizada com o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="87c1e-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="87c1e-106">O spooler MAPI chama a função [RTFSync](rtfsync.md) de dentro de uma versão empacotada da mensagem que ele passa para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="87c1e-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="87c1e-107">O provedor de transporte salva as alterações feitas na mensagem chamando o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e, em seguida, o encaminha para o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="87c1e-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="87c1e-108">Quando o aplicativo cliente que reconhece RTF do destinatário abre a mensagem para exibir o texto, ele deve sincronizar o texto com a formatação e abrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), dependendo de qual propriedade está disponível.</span><span class="sxs-lookup"><span data-stu-id="87c1e-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="87c1e-109">**Para abrir uma mensagem, clientes com conhecimento RTF**</span><span class="sxs-lookup"><span data-stu-id="87c1e-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="87c1e-110">Chame **RTFSync** para sincronizar o texto da mensagem com a formatação se o armazenamento de mensagens não estiver ciente de RTF.</span><span class="sxs-lookup"><span data-stu-id="87c1e-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="87c1e-111">O RTF_SYNC_BODY_CHANGED sinalizador deve ser passado no parâmetro  _ulFlags_ se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver ausente ou definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="87c1e-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="87c1e-112">Clientes que trabalham com armazenamentos de mensagens com conhecimento RTF não precisam fazer a chamada **RTFSync** porque o armazenamento de mensagens cuida disso.</span><span class="sxs-lookup"><span data-stu-id="87c1e-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="87c1e-113">Chame [IMAPIProp::SaveChanges](imapiprop-savechanges.md) se o texto da mensagem tiver sido atualizado.</span><span class="sxs-lookup"><span data-stu-id="87c1e-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="87c1e-114">Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir **a** PR_RTF_COMPRESSED propriedade.</span><span class="sxs-lookup"><span data-stu-id="87c1e-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="87c1e-115">Se **PR_RTF_COMPRESSED** não estiver disponível, você deve abrir a propriedade **PR_BODY** para exibir o conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="87c1e-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="87c1e-116">Chame a [função WrapCompressedRTFStream](wrapcompressedrtfstream.md) para criar uma versão descompactada dos dados RTF compactados, se disponível.</span><span class="sxs-lookup"><span data-stu-id="87c1e-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="87c1e-117">Exibe os dados RTF não compactados ou os dados de texto sem texto para o usuário.</span><span class="sxs-lookup"><span data-stu-id="87c1e-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="87c1e-118">**RTFSync** retorna um valor Boolean que indica se a mensagem foi atualizada ou não.</span><span class="sxs-lookup"><span data-stu-id="87c1e-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="87c1e-119">Se esse valor retornar TRUE, chame **SaveChanges** em algum momento para tornar a atualização permanente.</span><span class="sxs-lookup"><span data-stu-id="87c1e-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="87c1e-120">A chamada não precisa ser feita imediatamente após **o RTFSync** retornar.</span><span class="sxs-lookup"><span data-stu-id="87c1e-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="87c1e-121">Como muitos componentes lidam com o texto formatado antes de você recebê-lo, há a possibilidade de corrupção.</span><span class="sxs-lookup"><span data-stu-id="87c1e-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="87c1e-122">Essa corrupção pode vir do provedor do armazenamento de mensagens, de um aplicativo de terceiros, de um gateway ou de um erro de transmissão.</span><span class="sxs-lookup"><span data-stu-id="87c1e-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

