---
title: Gerar e usar identificadores de entradas em provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 10634305130b0f465482cce025018d4929350513
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565449"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="cbf35-103">Gerar e usar identificadores de entradas em provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="cbf35-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="cbf35-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbf35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbf35-105">Quando uma nova pasta ou mensagem é criada em um armazenamento de mensagens, o provedor de armazenamento de mensagem deve atribuir esse objeto em um identificador de entrada para que os aplicativos clientes podem se referir a ele.</span><span class="sxs-lookup"><span data-stu-id="cbf35-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="cbf35-106">Provedores de armazenamento de mensagens podem reutilizar os identificadores de entrada de longo prazo expirado dos objetos excluídos ou criar novos identificadores.</span><span class="sxs-lookup"><span data-stu-id="cbf35-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="cbf35-107">Não há nenhum requisito de uma forma ou outro para provedores de armazenamento de mensagem; No entanto, se ele for viável, um provedor de armazenamento de mensagem sempre deve gerar novos identificadores de entrada de longo prazo para novos objetos, em vez da reutilizando as antigas.</span><span class="sxs-lookup"><span data-stu-id="cbf35-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="cbf35-108">Há problemas reutilizar os identificadores de entrada de curto prazo quando os objetos que se referem ao são excluídos.</span><span class="sxs-lookup"><span data-stu-id="cbf35-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="cbf35-109">O motivo para essa exclusão é que os clientes podem armazenar em cache identificadores de entrada, às vezes por longos períodos de tempo.</span><span class="sxs-lookup"><span data-stu-id="cbf35-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="cbf35-110">Se isso ocorrer e o provedor de armazenamento de mensagem reutilizar os identificadores de entrada, é possível para o identificador de entrada para se referir a um objeto diferente, quando o cliente abre o identificador de entrada que quando obteve seu primeiro o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="cbf35-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="cbf35-111">Se o provedor de armazenamento de mensagem não reutilizar os identificadores de entrada — ou pelo menos usa um esquema de geração de identificador de entrada que não se repete por um tempo muito longo — esse problema não é possível ocorrer.</span><span class="sxs-lookup"><span data-stu-id="cbf35-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="cbf35-112">Da mesma forma, os provedores de armazenamento de mensagem devem tentar preservar os identificadores de entrada para pastas e mensagens quando forem movidos no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="cbf35-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="cbf35-113">Se o provedor de armazenamento de mensagens pode fazer isso, referências a objetos no repositório não tornarão inválidas quando o objeto é movido para um local diferente no repositório.</span><span class="sxs-lookup"><span data-stu-id="cbf35-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbf35-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbf35-114">See also</span></span>

- [<span data-ttu-id="cbf35-115">Recursos de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="cbf35-115">Message Store Features</span></span>](message-store-features.md)

