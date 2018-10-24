---
title: Texto formatado em MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bfaa4fd5f561c8138461db6ce8b9033c2a75b96b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580625"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="5eec6-103">Texto formatado em MAPI</span><span class="sxs-lookup"><span data-stu-id="5eec6-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="5eec6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eec6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eec6-105">O texto de uma mensagem pode ser armazenado e transmitidas usando texto sem formatação ou texto formatado.</span><span class="sxs-lookup"><span data-stu-id="5eec6-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="5eec6-106">Texto formatado aumenta o texto da mensagem, alterar sua aparência com, por exemplo, uma ou mais fontes, tamanhos de fonte ou cores de texto.</span><span class="sxs-lookup"><span data-stu-id="5eec6-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="5eec6-107">É recomendável que todos os clientes e sempre que possível, todos os provedores de armazenamento de mensagens, suporte a texto formatado.</span><span class="sxs-lookup"><span data-stu-id="5eec6-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="5eec6-108">Com suporte para texto formatado em mensagens agrega valor melhorar a legibilidade de mensagem e fazendo o tratamento de mensagens mais fácil e eficiente.</span><span class="sxs-lookup"><span data-stu-id="5eec6-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="5eec6-109">Texto formatado pode ser implementado de diversas maneiras.</span><span class="sxs-lookup"><span data-stu-id="5eec6-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="5eec6-110">A maneira mais comum é com o Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="5eec6-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="5eec6-111">MAPI define três propriedades de transmittable para manter informações de texto da mensagem: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para o texto sem formatação, **PR_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) para HTML e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para o texto RTF que tiverem sido compactado.</span><span class="sxs-lookup"><span data-stu-id="5eec6-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="5eec6-112">Como a versão formatada de um texto de mensagem pode ser duas vezes tão grande quanto a versão sem a formatação, o texto RTF é compactado antes que sejam transferido com a mensagem e armazenado na propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="5eec6-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="5eec6-113">Quando é hora de exibir a mensagem na tela, é descompactado usando uma função do utilitário fornecida pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="5eec6-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="5eec6-114">MAPI define essas duas propriedades de texto de mensagem e mecanismos para conversão entre eles para que os clientes RTF reconhecimento podem interoperar com os clientes e os sistemas de mensagens que não têm suporte para texto formatado.</span><span class="sxs-lookup"><span data-stu-id="5eec6-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="5eec6-115">Sincronizar o texto e a formatação</span><span class="sxs-lookup"><span data-stu-id="5eec6-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="5eec6-116">Descreve como manter o texto da mensagem RTF sincronizado com a formatação.</span><span class="sxs-lookup"><span data-stu-id="5eec6-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="5eec6-117">Suporte formatado Text em mensagens de saída: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="5eec6-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="5eec6-118">Descreve as responsabilidades do aplicativo cliente para dar suporte a texto formatado em mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="5eec6-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="5eec6-119">Suporte formatado Text em mensagens de entrada: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="5eec6-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="5eec6-120">Descreve as responsabilidades do aplicativo cliente para dar suporte a texto formatado em mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="5eec6-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="5eec6-121">Suporte de texto formatado: Responsabilidades do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="5eec6-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="5eec6-122">Descreve as responsabilidades do repositório de mensagem para dar suporte a texto formatado.</span><span class="sxs-lookup"><span data-stu-id="5eec6-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="5eec6-123">Suporte de texto formatado: Processamento de anexos</span><span class="sxs-lookup"><span data-stu-id="5eec6-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="5eec6-124">Descreve como escolher onde os anexos são processados.</span><span class="sxs-lookup"><span data-stu-id="5eec6-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="5eec6-125">Suporte de texto formatado: Responsabilidades do Gateway</span><span class="sxs-lookup"><span data-stu-id="5eec6-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="5eec6-126">Descreve as responsabilidades do gateway para mensagens de texto formatado de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="5eec6-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

