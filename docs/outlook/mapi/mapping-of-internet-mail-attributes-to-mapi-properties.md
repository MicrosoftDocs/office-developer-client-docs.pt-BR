---
title: Mapeamento dos atributos de email da Internet para propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4d1bc5fc5a5e304d81ab4252a527d0e52b0d6e3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19768036"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="3e202-103">Mapeamento dos atributos de email da Internet para propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e202-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="3e202-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e202-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e202-105">Este apêndice descreve como um provedor de transporte MAPI ou gateway reconhecimento de MAPI que se conecta à Internet deve traduzir entre os atributos de mensagem do protocolo de transporte de email simples (SMTP) e propriedades de mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e202-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="3e202-106">SMTP é o protocolo de mensagens usado em grande parte da Internet.</span><span class="sxs-lookup"><span data-stu-id="3e202-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="3e202-107">SMTP define um conjunto de cabeçalhos de mensagem — o envelope da mensagem — e um formato de conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3e202-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="3e202-108">SMTP está documentada em um conjunto de dois documentos, RFC 821 e RFC 822, que pode ser encontrado em um número de sites FTP e WWW na Internet.</span><span class="sxs-lookup"><span data-stu-id="3e202-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="3e202-109">Para obter informações sobre o protocolo SMTP usado para se comunicar com os agentes de email baseados em SMTP, consulte RFC 821, "Simple Mail Transfer Protocol," em [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="3e202-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="3e202-110">Para cabeçalhos de mensagem padrão e endereçamento, consulte RFC 822, "Padrão para o formato de ARPA Internet Text Messages," em [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="3e202-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="3e202-111">Para MIME, consulte RFC 1521, "parte MIME (Multipurpose Internet Mail Extensions) um: mecanismos para especificando e descrevendo o formato dos corpos de mensagens da Internet," em [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="3e202-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="3e202-112">O objetivo do mapeamento de atributos de mensagem SMTP para propriedades MAPI (e vice-versa) é garantir que todo o conteúdo das mensagens MAPI, além do que o que pode ser codificada atributos de mensagem SMTP nativos, pode ser trocado confiável entre diferente MAPI componentes que devem se comunicar pela Internet.</span><span class="sxs-lookup"><span data-stu-id="3e202-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="3e202-113">Este documento baseia-se no trabalho já realizado em tais componentes na Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e202-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="3e202-114">Este documento pressupõe familiaridade com transportes MAPI, TNEF e SMTP mail.</span><span class="sxs-lookup"><span data-stu-id="3e202-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="3e202-115">Ela se esforça para ser conciso em vez de muito claro.</span><span class="sxs-lookup"><span data-stu-id="3e202-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="3e202-116">Como uma convenção, "saída" refere-se para viagem de um UA compatível com MAPI ou MTA à Internet de email e "entrada" refere-se ao correio viajar da Internet para um componente MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e202-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

