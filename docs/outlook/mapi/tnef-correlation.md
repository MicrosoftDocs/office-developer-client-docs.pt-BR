---
title: Correlação de TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Última modificação: 12 de março de 2013'
ms.openlocfilehash: b8b30dcc2fcf0c8e75004e36b6fd9f4f4583e304
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770606"
---
# <a name="tnef-correlation"></a><span data-ttu-id="10fe3-103">Correlação de TNEF</span><span class="sxs-lookup"><span data-stu-id="10fe3-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="10fe3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10fe3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10fe3-105">Alguns sistemas de mensagens realizar uma verificação de correlação em qualquer fluxo Transport-Neutral Encapsulation Format (TNEF) anexado a uma mensagem de entrada para verificar que o fluxo TNEF na verdade pertencer a mensagem.</span><span class="sxs-lookup"><span data-stu-id="10fe3-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="10fe3-106">Isso envolve a correspondência com o valor de algum campo no cabeçalho da mensagem de entrada com uma cópia do valor armazenado na algumas propriedade no stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="10fe3-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="10fe3-107">Valores que são provavelmente exclusivos para cada mensagem, como números de identificação de mensagem, geralmente são usados para isso.</span><span class="sxs-lookup"><span data-stu-id="10fe3-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="10fe3-108">O transporte ou um gateway que criou o fluxo TNEF é responsável por escolhendo um valor apropriado no cabeçalho da mensagem e fazer uma cópia em uma propriedade adequada antes de codificação de propriedades da mensagem de saída no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="10fe3-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="10fe3-109">Gateways ou transportes que recebem a mensagem podem extrair dessa propriedade do stream TNEF e verificar que seu valor corresponde ao valor do campo correspondente do cabeçalho na mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="10fe3-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="10fe3-110">Se os valores não coincidirem, o gateway ou transporte deve descartar o fluxo TNEF e apenas o envelope de mensagem nativo do processo.</span><span class="sxs-lookup"><span data-stu-id="10fe3-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="10fe3-111">Essas verificações são recomendável porque os clientes de email não baseado em MAPI podem anexar um arquivo que contém um fluxo TNEF de uma mensagem antiga para um encaminhamento ou até mesmo uma mensagem não relacionada; Se não estiver marcado, tal erro pode causar perda de texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="10fe3-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="10fe3-112">O valor do campo de cabeçalho escolhido deve ser exclusivo à mensagem.</span><span class="sxs-lookup"><span data-stu-id="10fe3-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="10fe3-113">Há nenhum campo de cabeçalho fixa para todos os sistemas de mensagens, como sistemas de mensagens diferentes utilizam campos de cabeçalho diferente, mas normalmente, o sistema de mensagens atribui um identificador exclusivo para a mensagem que é adequada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="10fe3-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="10fe3-114">Por exemplo, sistemas de SMTP usam geralmente cabeçalho MessageID, enquanto os sistemas de x. 400 geralmente usam o atributo IM_THIS_IPM.</span><span class="sxs-lookup"><span data-stu-id="10fe3-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

