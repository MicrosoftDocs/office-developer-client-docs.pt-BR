---
title: Manipula notificações do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413532"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="83569-103">Manipula notificações do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="83569-103">Handing address book notification</span></span>
  
<span data-ttu-id="83569-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83569-105">As notificações do livro de endereços permitem que um cliente saiba dos eventos que ocorrem em qualquer entrada do livro de endereços ou em uma entrada específica.</span><span class="sxs-lookup"><span data-stu-id="83569-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="83569-106">Você pode se registrar para essas notificações através do livro de endereços MAPI chamando [IAddrBook::Advise](iaddrbook-advise.md) ou por meio da hierarquia ou tabela de conteúdo de um contêiner de agendamento de endereço chamando [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="83569-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="83569-107">Especifique o identificador de entrada de um contêiner de agendamento de endereço, lista de distribuição ou usuário de mensagens se você estiver se registrando para notificações em uma entrada específica e NULL se estiver se registrando para notificações em todo o livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="83569-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="83569-108">O identificador de entrada deve representar um usuário de mensagens ou uma lista de distribuição em um contêiner de agendamento de endereços.</span><span class="sxs-lookup"><span data-stu-id="83569-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="83569-109">**IAddrBook::Advise** examina esse identificador de entrada para determinar qual provedor de agendamento é responsável pelo objeto correspondente e encaminha a chamada para o método [IABLogon::Advise](iablogon-advise.md) do provedor de agendamento apropriado.</span><span class="sxs-lookup"><span data-stu-id="83569-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="83569-110">Os clientes podem se registrar para os seguintes tipos de eventos nas entradas do livro de endereços:</span><span class="sxs-lookup"><span data-stu-id="83569-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="83569-111">Erro crítico</span><span class="sxs-lookup"><span data-stu-id="83569-111">Critical error</span></span>
    
- <span data-ttu-id="83569-112">Qualquer um dos eventos de objeto (criados, modificados, excluídos, movidos ou copiados)</span><span class="sxs-lookup"><span data-stu-id="83569-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="83569-113">Tabela modificada</span><span class="sxs-lookup"><span data-stu-id="83569-113">Table modified</span></span>
    
<span data-ttu-id="83569-114">Normalmente, o registro ocorre apenas nos conteúdos do contêiner do address book e nas tabelas de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="83569-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="83569-115">É raro que os clientes se registrem com os objetos de lista de distribuição e usuário de mensagens de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="83569-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="83569-116">Isso porque:</span><span class="sxs-lookup"><span data-stu-id="83569-116">This is because:</span></span>
  
- <span data-ttu-id="83569-117">Muitos provedores de agendamento de endereço não suportam notificações em suas listas de distribuição e usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="83569-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="83569-118">As notificações de tabela são suficientes para rastrear alterações e re reportá-las aos usuários.</span><span class="sxs-lookup"><span data-stu-id="83569-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

