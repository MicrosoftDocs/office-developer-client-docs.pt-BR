---
title: Visão geral do provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767974"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="dcdf6-103">Visão geral do provedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="dcdf6-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="dcdf6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcdf6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcdf6-105">Provedores de transporte tratar recepção e transmissão de mensagens e implementam a segurança, se necessário.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="dcdf6-106">Eles também cuidam de qualquer pré-processamento necessário e tarefas de pós-processamento.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="dcdf6-107">Não há provedor de transporte normalmente uma para cada sistema de mensagens ativas.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="dcdf6-108">Aplicativos cliente se comunicar com o provedor de transporte por meio de um provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="dcdf6-109">Provedores de transporte registram com MAPI para lidar com um ou mais tipos de entradas de destinatário específicos.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="dcdf6-110">Quando uma mensagem está pronta para ser enviada, MAPI deve determinar qual provedor de transporte deve lidar com a transmissão.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="dcdf6-111">Dependendo do tipo de destinatário, MAPI, até mesmo, pode chamar após a mais de um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="dcdf6-112">Se um provedor de transporte indisponível for a única pessoa que pode lidar com o destinatário, a transmissão de mensagens será adiada até que uma conexão com esse provedor pode ser restabelecida.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="dcdf6-113">Alguns sistemas de mensagens são sistemas seguros; todos os usuários possíveis precisarão inserir um conjunto de credenciais válidas antes de acesso é permitido.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="dcdf6-114">MAPI impede o acesso não autorizado a tais sistemas de mensagens seguros fazendo com que o provedor de transporte validar as credenciais no momento do logon.</span><span class="sxs-lookup"><span data-stu-id="dcdf6-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

