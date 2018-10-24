---
title: Correlação de TNEF em transportes e gateways SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8192646007e8935a750a70e46b8210eebbc353f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578532"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="01988-103">Correlação de TNEF em transportes e gateways SMTP</span><span class="sxs-lookup"><span data-stu-id="01988-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="01988-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01988-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01988-105">Gateways e transportes que se conectam à internet com base em sistemas, aqueles que usam SMTP, use o valor das propriedades de cabeçalho SMTP MessageID e **PR_TNEF_CORRELATION_KEY** implementar correlação TNEF.</span><span class="sxs-lookup"><span data-stu-id="01988-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="01988-106">O valor do cabeçalho da mensagem de saída MessageID deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) e codificado no atributo [attMAPIProps](attmapiprops.md) do stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="01988-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="01988-107">Observe que **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, enquanto o MessageID é uma cadeia de caracteres; o terminador null deve ser incluído na cópia e na comparação.</span><span class="sxs-lookup"><span data-stu-id="01988-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="01988-108">Essa técnica é usada pelo software da Microsoft que se conecta com base em MAPI de sistemas de mensagens da Internet, como o Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="01988-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="01988-109">Essa técnica deve ser usada por qualquer gateways de SMTP e transportes que se conectam aos sistemas que oferecem suporte a clientes MAPI para maximizar a interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="01988-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

