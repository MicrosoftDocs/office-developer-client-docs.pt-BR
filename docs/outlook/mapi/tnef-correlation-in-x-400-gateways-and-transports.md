---
title: Correlação de TNEF em transportes e gateways X.400
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ea5ca41ef21c72377ade72370e0aee1b313c92d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770602"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="98c4d-103">Correlação de TNEF em transportes e gateways X.400</span><span class="sxs-lookup"><span data-stu-id="98c4d-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="98c4d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98c4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98c4d-105">Gateways e transportes que se conectam ao sistemas baseados em x. 400, use o valor do atributo IM_THIS_IPM 400 e o atributo TNEF **attMessageID** para implementar correlação TNEF.</span><span class="sxs-lookup"><span data-stu-id="98c4d-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="98c4d-106">O valor do atributo IM_THIS_IPM da mensagem de saída é copiado para **attMessageID** no stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="98c4d-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="98c4d-107">O atributo IM_THIS_IPM 400 geralmente é uma cadeia de caracteres, enquanto o atributo TNEF **attMessageID** é uma cadeia de caracteres de dígitos hexadecimais representando um valor binário.</span><span class="sxs-lookup"><span data-stu-id="98c4d-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="98c4d-108">Portanto, cada caractere no atributo IM_THIS_IPM 400, incluindo o caractere de terminação null, deve ser convertido em uma sequência de 2 caracteres hexadecimal que representa o valor ASCII do caractere.</span><span class="sxs-lookup"><span data-stu-id="98c4d-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="98c4d-109">Por exemplo, se o atributo de x. 400 do IM_THIS_IPM é a cadeia de caracteres a seguir:</span><span class="sxs-lookup"><span data-stu-id="98c4d-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="98c4d-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="98c4d-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="98c4d-111">em seguida, o valor da **attMessageID** seria a seguinte sequência de dígitos hexadecimais:</span><span class="sxs-lookup"><span data-stu-id="98c4d-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="98c4d-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="98c4d-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="98c4d-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="98c4d-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="98c4d-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="98c4d-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="98c4d-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="98c4d-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="98c4d-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="98c4d-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="98c4d-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="98c4d-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="98c4d-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="98c4d-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="98c4d-119">Essa técnica é usada pelo Microsoft Exchange Server x. 400 Connector.</span><span class="sxs-lookup"><span data-stu-id="98c4d-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="98c4d-120">Essa técnica deve ser usada por qualquer gateways x. 400 e transportes que se conectar ao Microsoft Exchange Server para maximizar a interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="98c4d-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="98c4d-121">Para melhor compatibilidade com o software Microsoft futuro bem como presente, o atributo IM_THIS_IPM 400 também deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98c4d-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="98c4d-122">No entanto, como **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, nenhuma tradução em uma cadeia de caracteres hexadecimal é necessária.</span><span class="sxs-lookup"><span data-stu-id="98c4d-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

