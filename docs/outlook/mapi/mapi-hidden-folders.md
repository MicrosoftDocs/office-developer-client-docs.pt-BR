---
title: Pastas ocultas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f9daa2169a087cf962d09a7c135e2829c7cd1ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346743"
---
# <a name="mapi-hidden-folders"></a><span data-ttu-id="c31d1-103">Pastas ocultas MAPI</span><span class="sxs-lookup"><span data-stu-id="c31d1-103">MAPI Hidden Folders</span></span>

  
  
<span data-ttu-id="c31d1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c31d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c31d1-105">As pastas ocultas são pastas genéricas criadas pelos clientes na pasta raiz do repositório de mensagens, e não na pasta raiz de uma subárvore de mensagem interpessoal (IPM).</span><span class="sxs-lookup"><span data-stu-id="c31d1-105">Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree.</span></span> <span data-ttu-id="c31d1-106">Como essas pastas não são colocadas em uma sub-árvore IPM, elas geralmente ficam ocultas da exibição do usuário pelo provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c31d1-106">Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider.</span></span> <span data-ttu-id="c31d1-107">As pastas ocultas normalmente contêm informações relevantes para o repositório de mensagens, mas irrelevante para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c31d1-107">Hidden folders typically contain information that is relevant to the message store but irrelevant to the user.</span></span> <span data-ttu-id="c31d1-108">Os clientes criam pastas ocultas para armazenar, por exemplo, informações adicionais a serem salvas com o restante da hierarquia de pastas.</span><span class="sxs-lookup"><span data-stu-id="c31d1-108">Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.</span></span>
  
<span data-ttu-id="c31d1-109">O MAPI espera que todos os clientes possam exibir, criar, modificar e excluir pastas em uma sub-árvore IPM.</span><span class="sxs-lookup"><span data-stu-id="c31d1-109">MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree.</span></span> <span data-ttu-id="c31d1-110">O suporte para trabalhar com pastas em outras árvores é considerado opcional.</span><span class="sxs-lookup"><span data-stu-id="c31d1-110">Support for working with folders in other trees is considered optional.</span></span> <span data-ttu-id="c31d1-111">No enTanto, todos os repositórios de mensagens que podem ser usados como o repositório padrão e que podem enviar e receber mensagens devem suportar totalmente as pastas ocultas.</span><span class="sxs-lookup"><span data-stu-id="c31d1-111">However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c31d1-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="c31d1-112">See also</span></span>



[<span data-ttu-id="c31d1-113">Pastas MAPI</span><span class="sxs-lookup"><span data-stu-id="c31d1-113">MAPI Folders</span></span>](mapi-folders.md)

