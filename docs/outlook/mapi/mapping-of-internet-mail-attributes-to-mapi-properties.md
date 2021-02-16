---
title: Mapeamento de atributos de email da Internet para propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355815"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="165e8-103">Mapeamento de atributos de email da Internet para propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="165e8-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="165e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="165e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="165e8-105">Este apêndice descreve como um provedor de transporte MAPI ou gateway com conhecimento mapi que se conecta à Internet deve ser traduzido entre propriedades de mensagem MAPI e atributos de mensagem SMTP.</span><span class="sxs-lookup"><span data-stu-id="165e8-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="165e8-106">SMTP é o protocolo de mensagens usado em grande parte da Internet.</span><span class="sxs-lookup"><span data-stu-id="165e8-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="165e8-107">SMTP define um conjunto de títulos de mensagem — o envelope da mensagem — e um formato de conteúdo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="165e8-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="165e8-108">O SMTP está totalmente documentado em um conjunto de dois documentos, RFC 821 e RFC 822, que podem ser encontrados em vários sites FTP e WWW na Internet.</span><span class="sxs-lookup"><span data-stu-id="165e8-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="165e8-109">Para obter informações sobre o protocolo SMTP usado para se comunicar com agentes de email baseados em SMTP, consulte RFC 821, "Simple Mail Transfer Protocol", em [https://www.rfc-editor.org](https://www.rfc-editor.org) .</span><span class="sxs-lookup"><span data-stu-id="165e8-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="165e8-110">Para endereçamento e os headers de mensagens padrão, consulte RFC 822, "Standard for the Format of ARPA Internet Text Messages", em [https://www.rfc-editor.org](https://www.rfc-editor.org) .</span><span class="sxs-lookup"><span data-stu-id="165e8-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="165e8-111">Para MIME, consulte RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Parte Um: Mecanismos para especificar e descrever o formato de corpos de mensagens da Internet", em [https://www.rfc-editor.org](https://www.rfc-editor.org) .</span><span class="sxs-lookup"><span data-stu-id="165e8-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="165e8-112">O objetivo do mapeamento de atributos de mensagem SMTP para propriedades MAPI (e vice-versa) é garantir que todo o conteúdo das mensagens MAPI, acima e acima do que possa ser codificado usando atributos de mensagem SMTP nativos, possa ser trocado de forma confiável entre diferentes componentes MAPI que devem se comunicar pela Internet.</span><span class="sxs-lookup"><span data-stu-id="165e8-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="165e8-113">Este documento se baseia no trabalho já realizado em tais componentes na Microsoft.</span><span class="sxs-lookup"><span data-stu-id="165e8-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="165e8-114">Este documento assume a familiaridade com os emails de transporte MAPI, TNEF e SMTP.</span><span class="sxs-lookup"><span data-stu-id="165e8-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="165e8-115">Ele se esforça para ser conciso em vez de ser claramente claro.</span><span class="sxs-lookup"><span data-stu-id="165e8-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="165e8-116">Como convenção, "saída" refere-se a emails que viajam de um UA ou MTA compatível com MAPI para a Internet, e "entrada" refere-se a emails que viajam da Internet para um componente MAPI.</span><span class="sxs-lookup"><span data-stu-id="165e8-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

