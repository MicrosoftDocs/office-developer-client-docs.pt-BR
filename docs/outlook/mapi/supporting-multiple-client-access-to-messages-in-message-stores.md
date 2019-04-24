---
title: Suporte a várias mensagens de acesso para cliente em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350600"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="f8cb8-103">Suporte a várias mensagens de acesso para cliente em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="f8cb8-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="f8cb8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8cb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8cb8-105">É possível que vários aplicativos cliente abram uma determinada mensagem simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-105">It is possible for multiple client applications to open a given message simultaneously.</span></span> <span data-ttu-id="f8cb8-106">Os provedores de repositórios de mensagens não precisam seguir regras específicas para o controle desse acesso.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-106">Message store providers do not have to follow any particular rules for governing such access.</span></span> <span data-ttu-id="f8cb8-107">No enTanto, se os aplicativos cliente modificarem a mensagem e salvar suas alterações, o provedor de repositório deverá estar em conformidade com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="f8cb8-107">However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="f8cb8-108">Permita que a primeira chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) prossiga como se fosse o único cliente com a mensagem aberta.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="f8cb8-109">Nas chamadas de **SaveChanges** subsequentes por outros clientes, o provedor de repositório de mensagens deve ignorar as alterações e retornar MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="f8cb8-110">Permitir que os aplicativos cliente respondam a um código de retorno do MAPI_E_OBJECT_CHANGED chamando o **SaveChanges** novamente com o sinalizador FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-110">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag.</span></span> <span data-ttu-id="f8cb8-111">Se um aplicativo cliente fizer isso, o provedor do repositório de mensagens deverá substituir as alterações anteriores pelas novas.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-111">If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="f8cb8-112">Como alternativa, o provedor do repositório de mensagens pode detectar o conflito e apresentar uma interface que permite ao usuário escolher se deseja manter a mensagem original, sobrescrever a mensagem original com as novas alterações ou salvar as novas alterações em outro local.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8cb8-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8cb8-113">See also</span></span>



[<span data-ttu-id="f8cb8-114">Implementar mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="f8cb8-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

