---
title: Suporte a texto formatado em mensagens de saída responsabilidades do cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431600"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="717e3-103">Suporte a texto formatado em mensagens de saída: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="717e3-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="717e3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="717e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="717e3-105">Os aplicativos cliente definem a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou a propriedade **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="717e3-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="717e3-106">Os clientes que oferecem suporte somente a texto sem formatação só definem a propriedade **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="717e3-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="717e3-107">Os clientes cientes do formato Rich Text (RTF) podem definir as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** , ou apenas **PR_RTF_COMPRESSED**, dependendo do provedor de armazenamento de mensagens que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="717e3-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="717e3-108">Clientes com reconhecimento de HTML definem a propriedade **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="717e3-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="717e3-109">É importante que um cliente Verifique sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do repositório de mensagens para determinar se o repositório suporta RTF.</span><span class="sxs-lookup"><span data-stu-id="717e3-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="717e3-110">Se o repositório de mensagens não reconhece o RTF, um cliente com reconhecimento de RTF define as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** para cada mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="717e3-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="717e3-111">Se o repositório de mensagens tiver reconhecimento de RTF, somente a propriedade **PR_RTF_COMPRESSED** precisará ser definida.</span><span class="sxs-lookup"><span data-stu-id="717e3-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="717e3-112">**Para definir PR_RTF_COMPRESSED e garantir que o processo de sincronização ocorra conforme necessário, os clientes com reconhecimento de RTF**</span><span class="sxs-lookup"><span data-stu-id="717e3-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="717e3-113">Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_RTF_COMPRESSED** , definindo os sinalizadores MAPI_CREATE e MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="717e3-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="717e3-114">O MAPI_CREATE garante que todos os novos dados substituam os dados antigos e o MAPI_MODIFY permite que você faça essas substituições.</span><span class="sxs-lookup"><span data-stu-id="717e3-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="717e3-115">Chame a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , passando STORE_UNCOMPRESSED_RTF se o repositório de mensagens define o bit STORE_UNCOMPRESSED_RTF em sua propriedade **PR_STORE_SUPPORT_MASK** , para obter uma versão descompactada do \*\*PR_RTF_COMPRESSED \*\*Stream retornado de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="717e3-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="717e3-116">Escreva os dados de texto da mensagem para o fluxo descompactado retornado de **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="717e3-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="717e3-117">Confirmar e liberar os fluxos não compactados e compactados.</span><span class="sxs-lookup"><span data-stu-id="717e3-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="717e3-118">Neste ponto, se o provedor do repositório de mensagens oferecer suporte a RTF, tudo isso é necessário.</span><span class="sxs-lookup"><span data-stu-id="717e3-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="717e3-119">Você pode depender do provedor de armazenamento de mensagens para lidar com o processo de sincronização e a criação da propriedade **PR_BODY** , se necessário.</span><span class="sxs-lookup"><span data-stu-id="717e3-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="717e3-120">No enTanto, se o provedor do repositório de mensagens não oferecer suporte a RTF, você deverá chamar a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação, definindo o sinalizador RTF_SYNC_RTF_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="717e3-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

