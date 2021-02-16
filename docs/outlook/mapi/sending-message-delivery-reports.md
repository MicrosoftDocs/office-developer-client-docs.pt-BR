---
title: Enviando relatórios de entrega de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433077"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="ff79b-103">Enviando relatórios de entrega de mensagens</span><span class="sxs-lookup"><span data-stu-id="ff79b-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="ff79b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff79b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff79b-105">Alguns sistemas de mensagens subjacentes suportam relatórios de entrega e outros não.</span><span class="sxs-lookup"><span data-stu-id="ff79b-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="ff79b-106">Como o provedor de transporte determina se os relatórios de entrega ou não de entrega de mensagens podem ser enviados aos aplicativos cliente é um detalhe de implementação específico para provedores de transporte individuais.</span><span class="sxs-lookup"><span data-stu-id="ff79b-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="ff79b-107">Se os relatórios de entrega puderem ser enviados a aplicativos cliente, os provedores de transporte usarão o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para notificar o MAPI de entrega bem-sucedida ou malsucedida para um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="ff79b-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="ff79b-108">EM seguida, o MAPI gera relatórios de entrega ou não entrega correspondentes a esses destinatários.</span><span class="sxs-lookup"><span data-stu-id="ff79b-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="ff79b-109">Os provedores de transporte também podem converter os relatórios de entrega de entrada e não entrega que são nativos para o sistema de mensagens em relatórios de entrega MAPI e sem entrega por meio de **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="ff79b-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

