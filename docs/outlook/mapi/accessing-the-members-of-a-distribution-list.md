---
title: Acessar os membros de uma lista de distribuição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a32552343fa90dfbbb3571f50846976a5f5f5edd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595360"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="dd9bc-103">Acessar os membros de uma lista de distribuição</span><span class="sxs-lookup"><span data-stu-id="dd9bc-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="dd9bc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd9bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="dd9bc-105">**Para obter os membros de uma lista de distribuição**</span><span class="sxs-lookup"><span data-stu-id="dd9bc-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="dd9bc-106">Criar uma matriz de marca de propriedade dimensionado com as propriedades dos membros que você deseja recuperar, como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dd9bc-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="dd9bc-107">Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir a lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="dd9bc-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="dd9bc-108">Chame o método de **IABContainer::GetContentsTable** da lista de distribuição para acessar sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="dd9bc-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="dd9bc-109">Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas da tabela que representa os membros da lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="dd9bc-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

