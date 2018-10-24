---
title: Abrir um descritor de modo de exibição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 680d80c0827399f3b7a0ea5819e51be654a05810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592476"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="d3fe1-103">Abrir um descritor de modo de exibição</span><span class="sxs-lookup"><span data-stu-id="d3fe1-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="d3fe1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3fe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3fe1-105">Muitas pastas podem ser abertas com um modo de exibição normal, um modo de exibição padrão ou qualquer número de exibições personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="d3fe1-106">Um modo de exibição descreve como exibir o conteúdo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="d3fe1-107">O modo de exibição normal é usado quando não há nenhum modo de exibição alternativo e quando você está abrindo a pasta pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="d3fe1-108">Quando houver um modo de exibição alternativo, você deve usá-lo para abrir a pasta.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="d3fe1-109">Um modo de exibição é descrito em uma mensagem conhecida como descritor de modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="d3fe1-110">Descritores de modo de exibição normalmente são criadas como mensagens associadas e podem aparecer nas pastas de exibição comuns ou pessoal ou em qualquer pasta IPM.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="d3fe1-111">Para abrir um descritor de modo de exibição</span><span class="sxs-lookup"><span data-stu-id="d3fe1-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="d3fe1-112">Chame [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para recuperar a tabela de conteúdo associado para a pasta.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="d3fe1-113">Criar uma restrição que localiza somente as mensagens com a classe de mensagem reservada para descritores de modo de exibição e chamar [IMAPITable:: Restrict](imapitable-restrict.md) para limitar a tabela e [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar as linhas apropriadas, ou …</span><span class="sxs-lookup"><span data-stu-id="d3fe1-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="d3fe1-114">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da pasta para recuperar sua propriedade **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d3fe1-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="d3fe1-115">**PR_DEFAULT_VIEW_ENTRYID** contém o identificador de entrada para a mensagem contendo o descritor de modo de exibição padrão para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="d3fe1-116">Essa chamada será bem-sucedida se a pasta dá suporte ao uso do sinalizador MAPI_ASSOCIATED em chamadas [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span><span class="sxs-lookup"><span data-stu-id="d3fe1-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="d3fe1-117">Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) com o identificador de entrada do descritor de modo de exibição para abri-lo.</span><span class="sxs-lookup"><span data-stu-id="d3fe1-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

