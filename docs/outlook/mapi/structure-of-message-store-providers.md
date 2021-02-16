---
title: Estrutura de provedores do armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426419"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="bd65b-103">Estrutura de provedores do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="bd65b-103">Structure of message store providers</span></span>
  
<span data-ttu-id="bd65b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd65b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd65b-105">Um provedor de armazenamento de mensagens, quando está sendo executado na memória, é um [IMSProvider : interface IUnknown.](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="bd65b-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="bd65b-106">A interface **IMSProvider** permite que aplicativos cliente e o spooler MAPI faça logoff de e para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bd65b-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="bd65b-107">As interfaces que os aplicativos cliente e o spooler MAPI usam para acessar pastas e mensagens no repositório de mensagens são interfaces [IMSLogon](imslogoniunknown.md) e [IMsgStore.](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="bd65b-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="bd65b-108">Normalmente, essas interfaces são criadas quando o armazenamento de mensagens é conectado pela primeira vez, embora o ponto de entrada [MSProviderInit](msproviderinit.md) da DLL do armazenamento de mensagens também possa criar.</span><span class="sxs-lookup"><span data-stu-id="bd65b-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="bd65b-109">Como as interfaces **IMSLogon** e **IMsgStore** compartilham alguns métodos, pode ser mais fácil criar um objeto de classe que herda de ambas as interfaces.</span><span class="sxs-lookup"><span data-stu-id="bd65b-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="bd65b-110">Você também pode implementar essas interfaces em objetos separados e gravar funções auxiliares internas à sua DLL que implementam os métodos compartilhados que podem ser chamados a partir dos métodos nas interfaces **IMSLogon** e **IMsgStore.**</span><span class="sxs-lookup"><span data-stu-id="bd65b-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="bd65b-111">A ilustração a seguir mostra uma delineada de alto nível da hierarquia de objetos em um armazenamento de mensagens em execução.</span><span class="sxs-lookup"><span data-stu-id="bd65b-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="bd65b-112">**Message store object hierarchy**</span><span class="sxs-lookup"><span data-stu-id="bd65b-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="bd65b-113">![Hierarquia de objetos do armazenamento de mensagens]Hierarquia de objetos do armazenamento de(media/storeobj.gif "mensagens")</span><span class="sxs-lookup"><span data-stu-id="bd65b-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd65b-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd65b-114">See also</span></span>

- [<span data-ttu-id="bd65b-115">Desenvolver um provedor de repositórios de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="bd65b-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

