---
title: Suporte a vários acesso do cliente para mensagens em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b13fbb9f2807c9814fed5ba3bcca8fe73aaa7b01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564217"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="3f43b-103">Suporte a vários acesso do cliente para mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="3f43b-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="3f43b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f43b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f43b-105">É possível para vários aplicativos de cliente abrir uma determinada mensagem simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="3f43b-105">It is possible for multiple client applications to open a given message simultaneously.</span></span> <span data-ttu-id="3f43b-106">Provedores de armazenamento de mensagem não precisará Siga todas as regras específicas para administrando tal acesso.</span><span class="sxs-lookup"><span data-stu-id="3f43b-106">Message store providers do not have to follow any particular rules for governing such access.</span></span> <span data-ttu-id="3f43b-107">No entanto, se os aplicativos cliente modificar a mensagem e salvem suas alterações, o provedor de armazenamento deve ser compatíveis com as regras a seguir:</span><span class="sxs-lookup"><span data-stu-id="3f43b-107">However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="3f43b-108">Permitir que a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) continuar como se fosse o único cliente que tem a mensagem aberto.</span><span class="sxs-lookup"><span data-stu-id="3f43b-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="3f43b-109">Sobre as chamadas subsequentes **SaveChanges** por outros clientes, o provedor de armazenamento de mensagem deve ignorar as alterações e retornar MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="3f43b-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="3f43b-110">Permitir aplicativos para responder a um código de retorno MAPI_E_OBJECT_CHANGED pela chamada **SaveChanges** novamente com o sinalizador FORCE_SAVE de cliente.</span><span class="sxs-lookup"><span data-stu-id="3f43b-110">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag.</span></span> <span data-ttu-id="3f43b-111">Se um aplicativo cliente faz isso, o provedor de armazenamento de mensagem deve substituir as alterações anteriores com os novos.</span><span class="sxs-lookup"><span data-stu-id="3f43b-111">If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="3f43b-112">Como alternativa, o provedor de armazenamento de mensagens pode detectar o conflito e apresentar uma interface que permite que o usuário escolha se deseja manter a mensagem original, substituir a mensagem original com as alterações ou salvar as alterações de novas para outro local.</span><span class="sxs-lookup"><span data-stu-id="3f43b-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f43b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f43b-113">See also</span></span>



[<span data-ttu-id="3f43b-114">Implementar mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="3f43b-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

