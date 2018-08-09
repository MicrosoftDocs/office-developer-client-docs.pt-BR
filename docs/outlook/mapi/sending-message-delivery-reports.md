---
title: Enviar relatórios de entrega de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770360"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="103a9-103">Enviar relatórios de entrega de mensagens</span><span class="sxs-lookup"><span data-stu-id="103a9-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="103a9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="103a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="103a9-105">Alguns sistemas de mensagens subjacentes ofereçam suporte a notificações de entrega e outros não.</span><span class="sxs-lookup"><span data-stu-id="103a9-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="103a9-106">Como o provedor de transporte determina se os relatórios de entrega ou não entrega de mensagem podem ser enviados para aplicativos cliente é um detalhe da implementação específico de provedores de transporte individual.</span><span class="sxs-lookup"><span data-stu-id="103a9-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="103a9-107">Se podem ser enviadas notificações de entrega para aplicativos clientes, provedores de transporte usam o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para notificar o MAPI de entrega ou não êxito para um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="103a9-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="103a9-108">MAPI, em seguida, gera relatórios de entrega ou NDRs correspondente a esses destinatários.</span><span class="sxs-lookup"><span data-stu-id="103a9-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="103a9-109">Provedores de transporte também podem converter a entrada relatórios de entrega e de não entrega são nativos do sistema de mensagens para entrega MAPI e NDRs por meio de **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="103a9-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

