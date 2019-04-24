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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="b320d-103">Mapeamento de atributos de email da Internet para propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b320d-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="b320d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b320d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b320d-105">Este apêndice descreve como um provedor de transporte MAPI ou um gateway ciente de MAPI que se conecta à Internet deve converter entre propriedades de mensagem MAPI e atributos de mensagem SMTP (Simple Mail Transport Protocol).</span><span class="sxs-lookup"><span data-stu-id="b320d-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="b320d-106">SMTP é o protocolo de mensagens usado em grande parte da Internet.</span><span class="sxs-lookup"><span data-stu-id="b320d-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="b320d-107">O SMTP define um conjunto de cabeçalhos de mensagem — o envelope da mensagem — e um formato de conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b320d-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="b320d-108">O SMTP está totalmente documentado em um conjunto de dois documentos, RFC 821 e RFC 822, que podem ser encontrados em vários sites FTP e WWW na Internet.</span><span class="sxs-lookup"><span data-stu-id="b320d-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="b320d-109">Para obter informações sobre o protocolo SMTP usado para se comunicar com agentes de email baseados em SMTP, consulte RFC 821, "Simple Mail Transfer Protocol [https://www.rfc-editor.org](https://www.rfc-editor.org)", em.</span><span class="sxs-lookup"><span data-stu-id="b320d-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="b320d-110">Para endereçamento e cabeçalhos de mensagem padrão, consulte RFC 822, "Standard for the formato of ARPA Internet text messages [https://www.rfc-editor.org](https://www.rfc-editor.org)" em.</span><span class="sxs-lookup"><span data-stu-id="b320d-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="b320d-111">Para MIME, consulte RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: mecanismos para especificar e descrever o formato de corpos de mensagens na Internet," [https://www.rfc-editor.org](https://www.rfc-editor.org)em.</span><span class="sxs-lookup"><span data-stu-id="b320d-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="b320d-112">O objetivo de mapear atributos de mensagens SMTP para propriedades MAPI (e vice-versa) é garantir que todo o conteúdo de mensagens MAPI, acima e acima, que possa ser codificada usando os atributos de mensagens SMTP nativos, possa ser trocado de forma confiável entre diferentes MAPI componentes que devem se comunicar pela Internet.</span><span class="sxs-lookup"><span data-stu-id="b320d-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="b320d-113">Este documento baseia-se no trabalho já realizado nesses componentes da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b320d-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="b320d-114">Este documento pressupõe familiaridade com transportes MAPI, TNEF e email SMTP.</span><span class="sxs-lookup"><span data-stu-id="b320d-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="b320d-115">Ele se esforça para ser conciso, em vez de claro.</span><span class="sxs-lookup"><span data-stu-id="b320d-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="b320d-116">Como uma convenção, "saída" refere-se a emails de um UA ou MTA compatíveis com MAPI para a Internet, e "entrada" refere-se a emails da Internet para um componente MAPI.</span><span class="sxs-lookup"><span data-stu-id="b320d-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

