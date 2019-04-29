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
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413035"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="e834a-103">Abrir um descritor de modo de exibição</span><span class="sxs-lookup"><span data-stu-id="e834a-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="e834a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e834a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e834a-105">Muitas pastas podem ser abertas com um modo de exibição normal, um modo de exibição padrão ou qualquer número de exibições personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e834a-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="e834a-106">Um modo de exibição descreve como exibir o conteúdo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="e834a-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="e834a-107">O modo de exibição normal é usado quando não há um modo de exibição alternativo e quando você está abrindo a pasta pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e834a-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="e834a-108">Quando um modo de exibição alternativo existe, você deve usá-lo para abrir a pasta.</span><span class="sxs-lookup"><span data-stu-id="e834a-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="e834a-109">Um modo de exibição é descrito em uma mensagem conhecida como um descritor de modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="e834a-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="e834a-110">Os descritores de modo geralmente são criados como mensagens associadas e podem aparecer nas pastas de exibição comum ou pessoal ou em qualquer pasta IPM.</span><span class="sxs-lookup"><span data-stu-id="e834a-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="e834a-111">Para abrir um descritor de modo de exibição</span><span class="sxs-lookup"><span data-stu-id="e834a-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="e834a-112">Chame [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable para recuperar a tabela de conteúdo associada da pasta.</span><span class="sxs-lookup"><span data-stu-id="e834a-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="e834a-113">Criar uma restrição que localiza somente mensagens com a classe de mensagem reservada para exibir descritores e Call [IMAPITable:: Restrict](imapitable-restrict.md) para limitar a tabela e IMAPITable [:: QueryRows](imapitable-queryrows.md) para recuperar as linhas apropriadas ou...</span><span class="sxs-lookup"><span data-stu-id="e834a-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="e834a-114">Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps da pasta para recuperar sua propriedade **PR_DEFAULT_VIEW_ENTRYID** ([pidtagdefaultviewentryid Canonical](pidtagdefaultviewentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e834a-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="e834a-115">**PR_DEFAULT_VIEW_ENTRYID** contém o identificador de entrada para a mensagem que contém o descritor de modo de exibição padrão de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="e834a-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="e834a-116">Essa chamada será bem-sucedida se a pasta suportar o uso do sinalizador MAPI_ASSOCIATED em chamadas para [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) e [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontenttable.</span><span class="sxs-lookup"><span data-stu-id="e834a-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="e834a-117">Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) com o identificador de entrada do descritor de modo de exibição para abri-lo.</span><span class="sxs-lookup"><span data-stu-id="e834a-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

