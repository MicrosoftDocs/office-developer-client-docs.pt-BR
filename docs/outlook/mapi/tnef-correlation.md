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
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410368"
---
# <a name="tnef-correlation"></a><span data-ttu-id="00ea2-103">Correlação de TNEF</span><span class="sxs-lookup"><span data-stu-id="00ea2-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="00ea2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00ea2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00ea2-105">Alguns sistemas de mensagens realizam uma verificação de correlação em qualquer fluxo de formato de encapsulamento de transporte neutro (TNEF) anexado a uma mensagem de entrada para verificar se o fluxo TNEF faz parte do fato pertence a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="00ea2-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="00ea2-106">Isso envolve a correspondência do valor de algum campo no cabeçalho da mensagem de entrada com uma cópia do valor armazenado em alguma propriedade no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="00ea2-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="00ea2-107">Os valores que são supostamente exclusivos para cada mensagem, como números de ID de mensagem, são normalmente usados para isso.</span><span class="sxs-lookup"><span data-stu-id="00ea2-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="00ea2-108">O transporte ou gateway que criou o fluxo TNEF é responsável por escolher um valor apropriado do cabeçalho da mensagem e colocar uma cópia em uma propriedade apropriada antes de codificar as propriedades da mensagem de saída no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="00ea2-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="00ea2-109">Gateways ou transportes que recebem a mensagem podem então extrair essa propriedade do fluxo TNEF e verificar se o valor corresponde ao valor do campo de cabeçalho correspondente na mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="00ea2-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="00ea2-110">Se os valores não corresponderem, o gateway ou transporte deverá descartar o fluxo TNEF e processar apenas o envelope de mensagem nativo.</span><span class="sxs-lookup"><span data-stu-id="00ea2-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="00ea2-111">Essas verificações são prudentes porque clientes de email não baseados em MAPI podem anexar um arquivo que contém um fluxo TNEF de uma mensagem antiga para uma mensagem de encaminhamento ou até mesmo uma inrelacionada; Se não for selecionada, tal erro poderá causar a perda de texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="00ea2-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="00ea2-112">O valor do campo de cabeçalho escolhido deve ser exclusivo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="00ea2-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="00ea2-113">Não há nenhum campo de cabeçalho fixo para todos os sistemas de mensagens porque diferentes sistemas de mensagens usam diferentes campos de cabeçalho, mas geralmente o sistema de mensagens atribui um identificador exclusivo à mensagem que é adequada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="00ea2-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="00ea2-114">Por exemplo, os sistemas SMTP normalmente usam o cabeçalho MessageID, enquanto os sistemas X. 400 normalmente usam o atributo IM_THIS_IPM.</span><span class="sxs-lookup"><span data-stu-id="00ea2-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

