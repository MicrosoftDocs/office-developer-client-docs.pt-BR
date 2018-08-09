---
title: Estrutura de provedores de armazenamento de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2f78428b8067b7937e9bd2ee36934cc29a16bfb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770539"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="475cf-103">Estrutura de provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="475cf-103">Structure of message store providers</span></span>
  
<span data-ttu-id="475cf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="475cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="475cf-105">Um provedor de armazenamento de mensagem, quando ele está em execução na memória, é um [IMSProvider: IUnknown](imsprovideriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="475cf-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="475cf-106">A interface de **IMSProvider** permite que o cliente aplicativos e o spooler MAPI fazer logon e logoff de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="475cf-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="475cf-107">As interfaces que aplicativos cliente e o MAPI spooler usam para acessar mensagens no armazenamento de mensagens e pastas são interfaces [IMSLogon](imslogoniunknown.md) e [IMsgStore](imsgstoreimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="475cf-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="475cf-108">Estas interfaces geralmente são criados quando o armazenamento de mensagens é primeiro fazer logon, embora o ponto de entrada da mensagem [MSProviderInit](msproviderinit.md) armazenar DLL também pode criá-los.</span><span class="sxs-lookup"><span data-stu-id="475cf-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="475cf-109">Como as interfaces **IMSLogon** e **IMsgStore** compartilham alguns métodos, talvez seja mais fácil criar um objeto de classe que herda de duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="475cf-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="475cf-110">Você também pode implementar estas interfaces nos objetos separados e grave funções de auxiliar internas para sua DLL que implementam os métodos compartilhados que podem ser chamados depois dos métodos nas interfaces **IMSLogon** e **IMsgStore** .</span><span class="sxs-lookup"><span data-stu-id="475cf-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="475cf-111">A ilustração a seguir mostra uma estrutura de tópicos de alto nível da hierarquia do objeto dentro de um armazenamento de mensagens em execução.</span><span class="sxs-lookup"><span data-stu-id="475cf-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="475cf-112">**Message store object hierarchy**</span><span class="sxs-lookup"><span data-stu-id="475cf-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="475cf-113">![Hierarquia de objetos de armazenamento de mensagens] (media/storeobj.gif "Hierarquia de objetos de armazenamento de mensagens")</span><span class="sxs-lookup"><span data-stu-id="475cf-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="475cf-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="475cf-114">See also</span></span>

- [<span data-ttu-id="475cf-115">Desenvolver um provedor do repositório de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="475cf-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

