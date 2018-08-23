---
title: Notificação de catálogo de endereços de manusear
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b5428ccde0e16bd32408b2ea908f5c5522992fc9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582914"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="1a3fc-103">Notificação de catálogo de endereços de manusear</span><span class="sxs-lookup"><span data-stu-id="1a3fc-103">Handing address book notification</span></span>
  
<span data-ttu-id="1a3fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a3fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a3fc-105">Notificações de catálogo de endereços permitem que um cliente saiba de eventos que ocorrem com qualquer entrada do catálogo de endereços ou como uma entrada específica.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="1a3fc-106">Você pode registrar para essas notificações por meio do catálogo de endereços MAPI chamando [IAddrBook::Advise](iaddrbook-advise.md) ou hierarquia de um contêiner catálogo de endereços ou de tabela de conteúdo chamando [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="1a3fc-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="1a3fc-107">Especifique o identificador de entrada de um contêiner de catálogo de endereços, lista de distribuição ou mensagens de usuário, se você está registrando para notificações em uma entrada específica e NULL se registrando para notificações de catálogo de endereços inteira.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="1a3fc-108">O identificador de entrada deve representar um usuário de mensagens ou a lista de distribuição em um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="1a3fc-109">**IAddrBook::Advise** examina esse identificador de entrada para determinar qual endereço do provedor de catálogo é responsável pelo objeto correspondente e encaminha a chamada ao método de [IABLogon::Advise](iablogon-advise.md) do provedor de catálogo de endereço apropriado.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="1a3fc-110">Os clientes podem se inscrever para os seguintes tipos de eventos de entradas do catálogo de endereços:</span><span class="sxs-lookup"><span data-stu-id="1a3fc-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="1a3fc-111">Erro crítico</span><span class="sxs-lookup"><span data-stu-id="1a3fc-111">Critical error</span></span>
    
- <span data-ttu-id="1a3fc-112">Qualquer um dos eventos de objeto (criado, modificado, excluído, movido ou copiadas)</span><span class="sxs-lookup"><span data-stu-id="1a3fc-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="1a3fc-113">Tabela modificada</span><span class="sxs-lookup"><span data-stu-id="1a3fc-113">Table modified</span></span>
    
<span data-ttu-id="1a3fc-114">Normalmente, o registro ocorre apenas no conteúdo do recipiente de catálogo de endereços e tabelas de hierarquias.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="1a3fc-115">É rara que clientes registrar os objetos de usuário e a distribuição da lista de mensagens com nível inferior.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="1a3fc-116">Isso acontece porque:</span><span class="sxs-lookup"><span data-stu-id="1a3fc-116">This is because:</span></span>
  
- <span data-ttu-id="1a3fc-117">Muitos provedores de catálogo de endereços não dão suporte a notificações em suas mensagens de usuários e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="1a3fc-118">Notificações de tabela são suficientes para o controle de alterações e relatórios-las aos usuários.</span><span class="sxs-lookup"><span data-stu-id="1a3fc-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

