---
title: Visão geral do provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404572"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="bafa0-103">Visão geral do provedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="bafa0-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="bafa0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bafa0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bafa0-105">Os provedores de transporte lidam com a transmissão e a recepção de mensagens e implementam a segurança, se necessário.</span><span class="sxs-lookup"><span data-stu-id="bafa0-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="bafa0-106">Eles também cuidam de todas as tarefas de pré-processamento e pós-processamento necessárias.</span><span class="sxs-lookup"><span data-stu-id="bafa0-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="bafa0-107">Normalmente, há um provedor de transporte para cada sistema de mensagens ativo.</span><span class="sxs-lookup"><span data-stu-id="bafa0-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="bafa0-108">Os aplicativos cliente se comunicam com o provedor de transporte por meio de um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bafa0-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="bafa0-109">Os provedores de transporte se registram com MAPI para lidar com um ou mais tipos específicos de entradas de destinatário.</span><span class="sxs-lookup"><span data-stu-id="bafa0-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="bafa0-110">Quando uma mensagem estiver pronta para ser enviada, o MAPI deverá determinar qual provedor de transporte deve lidar com a transmissão.</span><span class="sxs-lookup"><span data-stu-id="bafa0-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="bafa0-111">Dependendo do tipo de destinatário, o MAPI pode até chamar mais de um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="bafa0-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="bafa0-112">Se um provedor de transporte indisponível for o único que possa manipular o destinatário, a transmissão da mensagem será adiada até que uma conexão com esse provedor possa ser restabelecida.</span><span class="sxs-lookup"><span data-stu-id="bafa0-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="bafa0-113">Alguns sistemas de mensagens são sistemas seguros; todos os usuários potenciais precisam inserir um conjunto de credenciais válidas antes que o acesso seja permitido.</span><span class="sxs-lookup"><span data-stu-id="bafa0-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="bafa0-114">O MAPI impede o acesso não autorizado a esses sistemas de mensagens seguros, fazendo com que o provedor de transporte valide credenciais no momento do logon.</span><span class="sxs-lookup"><span data-stu-id="bafa0-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

