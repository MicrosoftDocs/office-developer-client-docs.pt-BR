---
title: Suporte a pesquisas em provedores de repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425383"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="4b42c-103">Suporte a pesquisas em provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="4b42c-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="4b42c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b42c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b42c-105">Os aplicativos cliente freqüentemente têm alguns componentes de interface do usuário dedicados à pesquisa de mensagens em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4b42c-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="4b42c-106">Os critérios de pesquisa são especificados na interface [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) por meio dos métodos [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) e [IMAPIContainer:: GetSearchCriteria](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="4b42c-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="4b42c-107">Os clientes usam a propriedade **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) do objeto de repositório de mensagens para identificar a pasta raiz no repositório de mensagens que contém pastas para resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4b42c-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="4b42c-108">Em geral, a pasta de resultados de pesquisa é uma pasta no nível superior do repositório de mensagens que não faz parte da árvore de pastas IPM e é, portanto, oculta.</span><span class="sxs-lookup"><span data-stu-id="4b42c-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="4b42c-109">Se seu provedor de repositório de mensagens usa uma pasta de resultados de pesquisa permanente ou cria um quando um cliente abre o identificador de entrada armazenado na propriedade **PR_FINDER_ENTRYID** é um detalhe de implementação.</span><span class="sxs-lookup"><span data-stu-id="4b42c-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="4b42c-110">É um pouco mais fácil para o provedor de armazenamento de mensagens usar uma pasta permanente que é criada quando o repositório de mensagens é criado, pois isso evita a complicação de verificar o identificador de entrada sempre que qualquer pasta é aberta para ver se deve criar um pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4b42c-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="4b42c-111">No enTanto, nem todos os provedores de repositório de mensagens podem fazer isso; notavelmente, repositórios de mensagens somente leitura ou repositórios que fornecem uma interface MAPI para um banco de dados herdado geralmente não são permitidos ou não podem criar uma pasta de resultados de pesquisa permanente no mecanismo de armazenamento subjacente.</span><span class="sxs-lookup"><span data-stu-id="4b42c-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b42c-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b42c-112">See also</span></span>



[<span data-ttu-id="4b42c-113">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="4b42c-113">Message Store Features</span></span>](message-store-features.md)

