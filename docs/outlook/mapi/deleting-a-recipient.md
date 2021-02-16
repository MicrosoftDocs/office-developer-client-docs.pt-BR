---
title: Excluindo um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421043"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="c5a68-103">Excluindo um destinatário</span><span class="sxs-lookup"><span data-stu-id="c5a68-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="c5a68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5a68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c5a68-105">**Para remover uma ou mais entradas do livro de endereços de um contêiner modificável**</span><span class="sxs-lookup"><span data-stu-id="c5a68-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="c5a68-106">Chame o [método IABContainer::D eleteEntries,](iabcontainer-deleteentries.md) passando uma matriz de identificadores de entrada que representam as entradas do livro de endereços a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="c5a68-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="c5a68-107">**DeleteEntries** pode retornar um aviso, MAPI_W_PARTIAL_COMPLETION, para indicar que não foi possível excluir uma ou mais entradas.</span><span class="sxs-lookup"><span data-stu-id="c5a68-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="c5a68-108">Teste esse valor de retorno com a macro **HR_FAILED** e chame o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) do contêiner se mais informações sobre o problema for necessária.</span><span class="sxs-lookup"><span data-stu-id="c5a68-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="c5a68-109">Quando você mantém um ponteiro para a estrutura [ADRENTRY](adrentry.md) de uma entrada excluída em seu cache, você ainda poderá recuperar propriedades usando seu identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5a68-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="c5a68-110">Isso porque a entrada só é marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="c5a68-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="c5a68-111">O MAPI mantém um nível de acesso a essas entradas marcadas por design.</span><span class="sxs-lookup"><span data-stu-id="c5a68-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

