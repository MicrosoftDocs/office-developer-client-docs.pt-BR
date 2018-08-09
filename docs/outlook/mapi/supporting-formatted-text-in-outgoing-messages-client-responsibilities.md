---
title: Suporte de texto formatado em saída responsabilidades de cliente de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770519"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="8ffa8-103">Suporte a texto formatado em mensagens de saída: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="8ffa8-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="8ffa8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ffa8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ffa8-105">Aplicativos cliente defina a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou a propriedade **PR_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) para uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="8ffa8-106">Clientes com suporte apenas texto sem formatação definida apenas a propriedade **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="8ffa8-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="8ffa8-107">Formato Rich Text (RTF)-lembre-se os clientes podem definir ambas as propriedades **PR_RTF_COMPRESSED** e **PR_BODY** , ou apenas **PR_RTF_COMPRESSED**, dependendo da mensagem armazenar provedor que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="8ffa8-108">Clientes de HTML defina a propriedade **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="8ffa8-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="8ffa8-109">É importante para um cliente verificar a propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do seu armazenamento de mensagens para determinar se o repositório suporta RTF.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="8ffa8-110">Se o armazenamento de mensagens não for RTF reconhecimento, um cliente de reconhecimento de RTF define propriedades **PR_BODY** tanto o **PR_RTF_COMPRESSED** para cada mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="8ffa8-111">Se o armazenamento da mensagem for RTF reconhecimento, apenas a propriedade **PR_RTF_COMPRESSED** deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="8ffa8-112">**Para definir PR_RTF_COMPRESSED e certifique-se de que a sincronização processo ocorre à medida que os clientes necessários, reconhecimento de RTF**</span><span class="sxs-lookup"><span data-stu-id="8ffa8-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="8ffa8-113">Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** , definindo sinalizadores MAPI_CREATE tanto o MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="8ffa8-114">MAPI_CREATE garante que todos os dados novos substituem quaisquer dados antigos e MAPI_MODIFY permite que você faça as substituições.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="8ffa8-115">Chamar a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , passando STORE_UNCOMPRESSED_RTF se o armazenamento de mensagens define estará definido o bit STORE_UNCOMPRESSED_RTF em sua propriedade **PR_STORE_SUPPORT_MASK** , para obter uma versão descompactada do **PR_RTF_COMPRESSED **stream retornado da **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="8ffa8-116">Gravar os dados de texto de mensagem no fluxo descompactado retornado da **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="8ffa8-117">Confirmar e versão fluxos compactados e descompactados.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="8ffa8-118">Neste ponto, se o provedor de armazenamento de mensagem suporta RTF, você fez tudo o que é necessário.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="8ffa8-119">Você pode depender o provedor de armazenamento de mensagem para lidar com o processo de sincronização e a criação da propriedade **PR_BODY** , se necessário.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="8ffa8-120">No entanto, se o provedor de armazenamento de mensagens não oferece suporte a RTF, você deve chamar a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação, definindo o sinalizador RTF_SYNC_RTF_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="8ffa8-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

