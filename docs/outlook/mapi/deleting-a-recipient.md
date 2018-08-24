---
title: Excluir um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582942"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="35356-103">Excluir um destinatário</span><span class="sxs-lookup"><span data-stu-id="35356-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="35356-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35356-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="35356-105">**Para remover um ou mais entradas do catálogo de endereços de um contêiner modificável**</span><span class="sxs-lookup"><span data-stu-id="35356-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="35356-106">Chame o método [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , passando uma matriz de identificadores de entrada que representam as entradas do catálogo de endereços a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="35356-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="35356-107">**DeleteEntries** pode retornar um aviso, MAPI_W_PARTIAL_COMPLETION, para indicar que ele não foi possível excluir uma ou mais das entradas.</span><span class="sxs-lookup"><span data-stu-id="35356-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="35356-108">Testar esse valor de retorno à macro **HR_FAILED** e chame o método de [IMAPIProp::GetLastError](imapiprop-getlasterror.md) do contêiner se forem necessárias mais informações sobre o problema.</span><span class="sxs-lookup"><span data-stu-id="35356-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="35356-109">Quando você mantiver um ponteiro à estrutura [ADRENTRY](adrentry.md) de uma entrada excluído em seu cache, você ainda poderá recuperar as propriedades utilizando seu identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="35356-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="35356-110">Isso ocorre porque a entrada só é marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="35356-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="35356-111">MAPI mantém um nível de acesso a essas entradas marcadas por design.</span><span class="sxs-lookup"><span data-stu-id="35356-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

