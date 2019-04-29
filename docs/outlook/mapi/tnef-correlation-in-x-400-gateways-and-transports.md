---
title: Correlação de TNEF nos gateways X. 400 e transportes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406371"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="764e2-103">Correlação de TNEF nos gateways X. 400 e transportes</span><span class="sxs-lookup"><span data-stu-id="764e2-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="764e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="764e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="764e2-105">Gateways e transportes que se conectam a sistemas baseados em X. 400, usam o valor do atributo IM_THIS_IPM X. 400 e o atributo TNEF **attMessageID** para implementar a correlação de TNEF.</span><span class="sxs-lookup"><span data-stu-id="764e2-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="764e2-106">O valor do atributo IM_THIS_IPM da mensagem de saída é copiado para **attMessageID** no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="764e2-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="764e2-107">O atributo IM_THIS_IPM X. 400 geralmente é uma cadeia de caracteres, enquanto o atributo TNEF **attMessageID** é uma cadeia de caracteres de dígitos hexadecimais que representam um valor binário.</span><span class="sxs-lookup"><span data-stu-id="764e2-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="764e2-108">Portanto, cada caractere no atributo IM_THIS_IPM X. 400, incluindo o caractere nulo de terminação, deve ser convertido em uma cadeia de caracteres hexadecimal de 2 caracteres representando o valor ASCII desse caractere.</span><span class="sxs-lookup"><span data-stu-id="764e2-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="764e2-109">Por exemplo, se o atributo IM_THIS_IPM X. 400 for a cadeia de caracteres a seguir:</span><span class="sxs-lookup"><span data-stu-id="764e2-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="764e2-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="764e2-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="764e2-111">em seguida, o valor de **attMessageID** seria a seguinte sequência de dígitos hexadecimais:</span><span class="sxs-lookup"><span data-stu-id="764e2-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="764e2-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="764e2-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="764e2-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="764e2-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="764e2-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="764e2-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="764e2-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="764e2-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="764e2-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="764e2-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="764e2-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="764e2-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="764e2-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="764e2-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="764e2-119">Essa técnica é usada pelo conector do Microsoft Exchange Server X. 400.</span><span class="sxs-lookup"><span data-stu-id="764e2-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="764e2-120">Essa técnica deve ser usada por quaisquer Gateways X. 400 e transportes que se conectam ao Microsoft Exchange Server para maximizar a interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="764e2-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="764e2-121">Para obter maior compatibilidade com o futuro, bem como apresentar o software da Microsoft, o atributo IM_THIS_IPM X. 400 também deve ser copiado para a propriedade **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="764e2-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="764e2-122">No enTanto, como **PR_TNEF_CORRELATION_KEY** é uma propriedade binária, não é necessária nenhuma conversão em uma cadeia de caracteres hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="764e2-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

