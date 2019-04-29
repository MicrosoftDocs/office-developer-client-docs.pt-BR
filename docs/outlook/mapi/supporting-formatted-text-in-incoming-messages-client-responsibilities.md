---
title: Suporte a texto formatado em mensagens de entrada responsabilidades do cliente
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
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="83b0b-103">Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="83b0b-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="83b0b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83b0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83b0b-105">À medida que as mensagens são transferidas entre sistemas de mensagens, o spooler MAPI garante que a formatação rich text permaneça sincronizada com o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="83b0b-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="83b0b-106">O spooler MAPI chama a função [RTFSync](rtfsync.md) de dentro de uma versão empacotada da mensagem que passa para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="83b0b-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="83b0b-107">O provedor de transporte salva as alterações feitas na mensagem chamando o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) e, em seguida, encaminha-o para o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="83b0b-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="83b0b-108">Quando o aplicativo cliente de reconhecimento de RTF do destinatário abre a mensagem para exibir o texto, ele deve sincronizar o texto com a formatação e abrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , dependendo da propriedade que está disponível.</span><span class="sxs-lookup"><span data-stu-id="83b0b-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="83b0b-109">**Para abrir uma mensagem, clientes com reconhecimento de RTF**</span><span class="sxs-lookup"><span data-stu-id="83b0b-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="83b0b-110">Chame **RTFSync** para sincronizar o texto da mensagem com a formatação se o repositório de mensagens não reconhece o RTF.</span><span class="sxs-lookup"><span data-stu-id="83b0b-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="83b0b-111">O sinalizador RTF_SYNC_BODY_CHANGED deve ser passado no parâmetro _parâmetroulflags_ se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver ausente ou definida como false.</span><span class="sxs-lookup"><span data-stu-id="83b0b-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="83b0b-112">Os clientes que trabalham com armazenamento de mensagens com reconhecimento de RTF não precisam fazer a chamada **RTFSync** porque o repositório de mensagens cuida dela.</span><span class="sxs-lookup"><span data-stu-id="83b0b-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="83b0b-113">Chamar [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) se o texto da mensagem tiver sido atualizado.</span><span class="sxs-lookup"><span data-stu-id="83b0b-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="83b0b-114">Chame [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="83b0b-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="83b0b-115">Se **PR_RTF_COMPRESSED** não estiver disponível, você deve abrir a propriedade **PR_BODY** em vez de exibir o conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="83b0b-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="83b0b-116">Chame a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para criar uma versão descompactado dos dados RTF compactados, se disponível.</span><span class="sxs-lookup"><span data-stu-id="83b0b-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="83b0b-117">Exibe os dados RTF não compactados ou os dados de texto sem formatação para o usuário.</span><span class="sxs-lookup"><span data-stu-id="83b0b-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="83b0b-118">**RTFSync** retorna um valor Boolean que indica se a mensagem foi atualizada ou não.</span><span class="sxs-lookup"><span data-stu-id="83b0b-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="83b0b-119">Se esse valor retornar TRUE, chame **SaveChanges** em algum momento para tornar a atualização permanente.</span><span class="sxs-lookup"><span data-stu-id="83b0b-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="83b0b-120">A chamada não precisa ser feita imediatamente após o **RTFSync** retornar.</span><span class="sxs-lookup"><span data-stu-id="83b0b-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="83b0b-121">Como muitos componentes lidam com o texto formatado antes de ser recebido, há a possibilidade de corrupção.</span><span class="sxs-lookup"><span data-stu-id="83b0b-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="83b0b-122">Essa corrupção pode ser proveniente do provedor de armazenamento de mensagens, de um aplicativo de terceiros, de um gateway ou de um erro de transmissão.</span><span class="sxs-lookup"><span data-stu-id="83b0b-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

