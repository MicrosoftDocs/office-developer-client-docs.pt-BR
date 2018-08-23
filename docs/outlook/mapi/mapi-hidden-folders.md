---
title: Pastas ocultada de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 70aeda8789665a3f35bf75f83f32a92dbeedc8de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589102"
---
# <a name="mapi-hidden-folders"></a><span data-ttu-id="3a062-103">Pastas ocultada de MAPI</span><span class="sxs-lookup"><span data-stu-id="3a062-103">MAPI Hidden Folders</span></span>

  
  
<span data-ttu-id="3a062-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a062-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a062-105">Pastas ocultas são genéricas pastas criadas por clientes na pasta raiz do repositório de mensagem, em vez de na pasta raiz de uma subárvore interpessoais mensagens (IPM).</span><span class="sxs-lookup"><span data-stu-id="3a062-105">Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree.</span></span> <span data-ttu-id="3a062-106">Porque essas pastas não são colocadas em uma subárvore IPM, geralmente estão ocultos do modo de exibição do usuário pelo provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3a062-106">Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider.</span></span> <span data-ttu-id="3a062-107">Pastas ocultas normalmente contêm informações que são relevantes para o armazenamento de mensagens, mas é irrelevante para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3a062-107">Hidden folders typically contain information that is relevant to the message store but irrelevant to the user.</span></span> <span data-ttu-id="3a062-108">Os clientes criar pastas ocultas para armazenar, por exemplo, informações adicionais sejam salvos com o restante da hierarquia de pastas.</span><span class="sxs-lookup"><span data-stu-id="3a062-108">Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.</span></span>
  
<span data-ttu-id="3a062-109">MAPI espera que todos os clientes possam exibir, criar, modificar e excluir pastas em uma subárvore IPM.</span><span class="sxs-lookup"><span data-stu-id="3a062-109">MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree.</span></span> <span data-ttu-id="3a062-110">Suporte para trabalhar com pastas em outras árvores será considerado opcional.</span><span class="sxs-lookup"><span data-stu-id="3a062-110">Support for working with folders in other trees is considered optional.</span></span> <span data-ttu-id="3a062-111">No entanto, todos os repositórios de mensagem que pode ser usado como o armazenamento padrão e que podem enviar e receber mensagens totalmente devem oferecer suporte a pastas ocultas.</span><span class="sxs-lookup"><span data-stu-id="3a062-111">However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a062-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a062-112">See also</span></span>



[<span data-ttu-id="3a062-113">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="3a062-113">MAPI Folders</span></span>](mapi-folders.md)

