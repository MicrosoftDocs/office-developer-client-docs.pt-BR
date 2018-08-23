---
title: Suporte a pesquisas em provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f206623103f810b2868502aea7c6804cd306f022
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573191"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="9ac2d-103">Suporte a pesquisas em provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="9ac2d-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="9ac2d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ac2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ac2d-105">Aplicativos clientes frequentemente têm alguns componentes de interface do usuário devotados a pesquisar mensagens em um repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ac2d-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="9ac2d-106">Critérios de pesquisa são especificados no [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) interface por meio dos métodos [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) e [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="9ac2d-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="9ac2d-107">Clientes usam a mensagem repositório de propriedade do objeto **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) para identificar a pasta raiz no repositório de mensagem que contém pastas para os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ac2d-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="9ac2d-108">A pasta de resultados de pesquisa geralmente é uma pasta de nível superior do repositório de mensagem que não faz parte da árvore da pasta IPM e é, portanto, oculto.</span><span class="sxs-lookup"><span data-stu-id="9ac2d-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="9ac2d-109">Se o seu provedor de armazenamento de mensagem usa uma pasta de resultados de pesquisa permanente ou cria um quando um cliente abre o identificador de entrada armazenado na propriedade **PR_FINDER_ENTRYID** é um detalhe da implementação.</span><span class="sxs-lookup"><span data-stu-id="9ac2d-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="9ac2d-110">É relativamente mais fácil para seu provedor de armazenamento de mensagem usar uma pasta permanente que é criada quando o armazenamento de mensagens é criado, porque fazer isso evita a complexidade das verificando o identificador de entrada sempre que qualquer pasta é aberta para ver se é necessário criar um pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ac2d-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="9ac2d-111">No entanto, nem todos os provedores de armazenamento de mensagens podem fazer isso; em especial, repositórios de mensagem de somente leitura ou repositórios que fornecem uma interface MAPI para um banco de dados herdado geralmente não são permitidos ou não conseguem criar uma pasta de resultados de pesquisa permanente no mecanismo de armazenamento subjacente.</span><span class="sxs-lookup"><span data-stu-id="9ac2d-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ac2d-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ac2d-112">See also</span></span>



[<span data-ttu-id="9ac2d-113">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="9ac2d-113">Message Store Features</span></span>](message-store-features.md)

