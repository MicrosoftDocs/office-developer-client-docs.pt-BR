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
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437676"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="235b8-103">Gerar e usar identificadores de entradas em provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="235b8-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="235b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="235b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="235b8-105">Quando uma nova pasta ou mensagem é criada em um armazenamento de mensagens, o provedor de armazenamento de mensagens precisa atribuir a esse objeto um identificador de entrada para que os aplicativos clientes possam se referir a ele.</span><span class="sxs-lookup"><span data-stu-id="235b8-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="235b8-106">Os provedores de armazenamento de mensagens podem reutilizar os identificadores de entrada de longo prazo dos objetos excluídos ou criar novos identificadores.</span><span class="sxs-lookup"><span data-stu-id="235b8-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="235b8-107">Não há requisitos de uma maneira ou de outra para provedores de armazenamento de mensagens; No entanto, se for viável, um provedor de armazenamento de mensagens deve sempre gerar novos identificadores de entrada de longo prazo para novos objetos em vez de reutilizar os antigos.</span><span class="sxs-lookup"><span data-stu-id="235b8-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="235b8-108">Não há problema em reutilizar identificadores de entrada de curto prazo quando os objetos a que se referem são excluídos.</span><span class="sxs-lookup"><span data-stu-id="235b8-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="235b8-109">O motivo para essa exclusão é que os clientes podem armazenar em cache identificadores de entrada, às vezes por longos períodos de tempo.</span><span class="sxs-lookup"><span data-stu-id="235b8-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="235b8-110">Se isso acontecer e o provedor do armazenamento de mensagens reutilizar identificadores de entrada, é possível que o identificador de entrada se refira a um objeto diferente quando o cliente abre o identificador de entrada do que quando obteve pela primeira vez o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="235b8-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="235b8-111">Se o provedor do armazenamento de mensagens não reutilizar identificadores de entrada — ou pelo menos usar um esquema de geração de identificador de entrada que não se repete há muito tempo — esse problema não pode ocorrer.</span><span class="sxs-lookup"><span data-stu-id="235b8-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="235b8-112">Da mesma forma, os provedores de armazenamento de mensagens devem tentar preservar identificadores de entrada para pastas e mensagens quando eles são movidos no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="235b8-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="235b8-113">Se o provedor de armazenamento de mensagens puder fazer isso, as referências a objetos no armazenamento não se tornarão inválidas quando o objeto for movido para um local diferente no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="235b8-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="235b8-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="235b8-114">See also</span></span>

- [<span data-ttu-id="235b8-115">Recursos do Armazenamento de Mensagens</span><span class="sxs-lookup"><span data-stu-id="235b8-115">Message Store Features</span></span>](message-store-features.md)

