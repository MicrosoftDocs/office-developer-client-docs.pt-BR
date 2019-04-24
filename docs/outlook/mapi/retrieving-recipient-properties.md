---
title: Recuperar propriedades de destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279588"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="cf156-103">Recuperar propriedades de destinatários</span><span class="sxs-lookup"><span data-stu-id="cf156-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="cf156-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf156-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="cf156-105">Para acessar uma ou mais propriedades de uma entrada do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="cf156-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="cf156-106">Para cada entrada de catálogo de endereços de interesse, chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md), passando o identificador de entrada do usuário de mensagens de destino ou lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="cf156-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="cf156-107">Em seguida, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="cf156-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="cf156-108">Chame o usuário de mensagens ou a lista de distribuição do método [IMAPIProp::](imapiprop-getprops.md) GetProps para cada entrada de catálogo de endereços de interesse, com uma lista de uma ou mais propriedades a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="cf156-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="cf156-109">Call [IAddrBook::P reparerecips](iaddrbook-preparerecips.md), passando uma estrutura [das ADRLIST](adrlist.md) que contém todas as propriedades de todas as entradas do catálogo de endereços desejado.</span><span class="sxs-lookup"><span data-stu-id="cf156-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="cf156-110">Como uma chamada a **PrepareRecips** pode retornar informações para várias entradas do catálogo de endereços, ela é a estratégia preferida quando você está interessado em mais de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="cf156-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

