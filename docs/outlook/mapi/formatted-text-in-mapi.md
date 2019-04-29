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
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408086"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="22279-103">Texto formatado em MAPI</span><span class="sxs-lookup"><span data-stu-id="22279-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="22279-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22279-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22279-105">O texto de uma mensagem pode ser armazenado e transmitido usando texto sem formatação ou texto formatado.</span><span class="sxs-lookup"><span data-stu-id="22279-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="22279-106">O texto formatado aprimora o texto da mensagem alterando sua aparência com, por exemplo, uma ou mais fontes, tamanhos de fonte ou cores de texto.</span><span class="sxs-lookup"><span data-stu-id="22279-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="22279-107">É recomendável que todos os clientes e, sempre que possível, todos os provedores de repositórios de mensagens, ofereçam suporte ao texto formatado.</span><span class="sxs-lookup"><span data-stu-id="22279-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="22279-108">O suporte a texto formatado em mensagens agrega valor, melhorando a legibilidade da mensagem e tornando o tratamento de mensagens mais fácil e mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="22279-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="22279-109">O texto formatado pode ser implementado de diversas maneiras.</span><span class="sxs-lookup"><span data-stu-id="22279-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="22279-110">A maneira mais comum é com o formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="22279-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="22279-111">MAPI define três propriedades transmittable para armazenar informações de texto da mensagem: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para texto sem formatação, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para HTML e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para texto RTF que tenha sido compactado.</span><span class="sxs-lookup"><span data-stu-id="22279-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="22279-112">Como a versão formatada de um texto de mensagem pode ser duas vezes maior que a versão sem a formatação, o texto RTF é compactado antes de ser transferido com a mensagem e armazenado na propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="22279-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="22279-113">Quando é hora de exibir a mensagem na tela, ela é descompactada usando uma função de utilitário fornecida por MAPI.</span><span class="sxs-lookup"><span data-stu-id="22279-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="22279-114">O MAPI define essas duas propriedades e mecanismos de texto de mensagem para conversão entre eles de forma que os clientes com reconhecimento de RTF possam interoperar com clientes e sistemas de mensagens que não dão suporte a texto formatado.</span><span class="sxs-lookup"><span data-stu-id="22279-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="22279-115">Sincronização de texto e formatação</span><span class="sxs-lookup"><span data-stu-id="22279-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="22279-116">Descreve como manter o texto da mensagem RTF sincronizado com a formatação.</span><span class="sxs-lookup"><span data-stu-id="22279-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="22279-117">Suporte a texto formatado em mensagens de saída: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="22279-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="22279-118">Descreve as responsabilidades do aplicativo cliente para dar suporte ao texto formatado em mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="22279-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="22279-119">Suporte a texto formatado em mensagens de entrada: responsabilidades do cliente</span><span class="sxs-lookup"><span data-stu-id="22279-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="22279-120">Descreve as responsabilidades do aplicativo cliente para dar suporte ao texto formatado em mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="22279-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="22279-121">Suporte a texto formatado: responsabilidades do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="22279-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="22279-122">Descreve as responsabilidades do repositório de mensagens para dar suporte ao texto formatado.</span><span class="sxs-lookup"><span data-stu-id="22279-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="22279-123">Suporte a texto formatado: anexos de renderização</span><span class="sxs-lookup"><span data-stu-id="22279-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="22279-124">Descreve como escolher onde os anexos são renderizados.</span><span class="sxs-lookup"><span data-stu-id="22279-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="22279-125">Suporte a texto formatado: responsabilidades do gateway</span><span class="sxs-lookup"><span data-stu-id="22279-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="22279-126">Descreve as responsabilidades de gateway para mensagens de texto de saída e de entrada formatadas.</span><span class="sxs-lookup"><span data-stu-id="22279-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

