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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299500"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="fc296-103">Manipula notificações do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="fc296-103">Handing address book notification</span></span>
  
<span data-ttu-id="fc296-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc296-105">As notificações do catálogo de endereços permitem que um cliente Aprenda eventos que ocorrem a qualquer entrada do catálogo de endereços ou a uma entrada específica.</span><span class="sxs-lookup"><span data-stu-id="fc296-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="fc296-106">Você pode registrar essas notificações por meio do catálogo de endereços MAPI chamando [IAddrBook:: Advise](iaddrbook-advise.md) ou por meio de uma hierarquia de conteúdo do contêiner de catálogo de endereços ou tabela de conteúdo chamando IMAPITable [:: Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="fc296-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="fc296-107">Especifique o identificador de entrada de um contêiner de catálogo de endereços, lista de distribuição ou usuário de mensagens se você estiver se registrando para notificações em uma determinada entrada e nulo se estiver se registrando para notificações em todo o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="fc296-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="fc296-108">O identificador de entrada deve representar um usuário de mensagens ou uma lista de distribuição em um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="fc296-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="fc296-109">**IAddrBook:: Advise** examina esse identificador de entrada para determinar qual provedor de catálogo de endereços é responsável pelo objeto correspondente e encaminha a chamada para o método [IABLogon:: Advise](iablogon-advise.md) do provedor de catálogo de endereços apropriado.</span><span class="sxs-lookup"><span data-stu-id="fc296-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="fc296-110">Os clientes podem se registrar nos seguintes tipos de eventos nas entradas do catálogo de endereços:</span><span class="sxs-lookup"><span data-stu-id="fc296-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="fc296-111">Erro crítico</span><span class="sxs-lookup"><span data-stu-id="fc296-111">Critical error</span></span>
    
- <span data-ttu-id="fc296-112">Qualquer um dos eventos de objeto (criado, modificado, excluído, movido ou copiado)</span><span class="sxs-lookup"><span data-stu-id="fc296-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="fc296-113">Tabela modificada</span><span class="sxs-lookup"><span data-stu-id="fc296-113">Table modified</span></span>
    
<span data-ttu-id="fc296-114">Normalmente, o registro ocorre somente no conteúdo do contêiner do catálogo de endereços e tabelas de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="fc296-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="fc296-115">É raro que os clientes sejam registrados com o usuário de sistema de mensagens de nível inferior e os objetos de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="fc296-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="fc296-116">Isso ocorre porque:</span><span class="sxs-lookup"><span data-stu-id="fc296-116">This is because:</span></span>
  
- <span data-ttu-id="fc296-117">Muitos provedores de catálogo de endereços não dão suporte a notificações em seus usuários de mensagens e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="fc296-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="fc296-118">As notificações de tabela são suficientes para controlar alterações e relatá-las aos usuários.</span><span class="sxs-lookup"><span data-stu-id="fc296-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

