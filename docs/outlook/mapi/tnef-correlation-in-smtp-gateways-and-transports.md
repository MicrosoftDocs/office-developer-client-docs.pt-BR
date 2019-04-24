---
title: Correlação de TNEF em gateways e transportes SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339687"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="da36b-103">Correlação de TNEF em gateways e transportes SMTP</span><span class="sxs-lookup"><span data-stu-id="da36b-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="da36b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da36b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da36b-105">Gateways e transportes que se conectam a sistemas baseados na Internet, aqueles que usam SMTP, usam o valor do cabeçalho SMTP MessageID e a propriedade **PR_TNEF_CORRELATION_KEY** para implementar a correlação de TNEF.</span><span class="sxs-lookup"><span data-stu-id="da36b-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="da36b-106">O valor do cabeçalho MessageID da mensagem de saída deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) e codificado no atributo [attMAPIProps](attmapiprops.md) do fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="da36b-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="da36b-107">Observe que **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, enquanto MessageId é uma cadeia de caracteres; o terminador NULL deve ser incluído na cópia e na comparação.</span><span class="sxs-lookup"><span data-stu-id="da36b-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="da36b-108">Essa técnica é usada por todos os softwares da Microsoft que conectam sistemas de mensagens baseados em MAPI à Internet, como o Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="da36b-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="da36b-109">Essa técnica deve ser usada por quaisquer gateways SMTP e transportes que se conectam a sistemas que dão suporte a clientes MAPI para maximizar a interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="da36b-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

