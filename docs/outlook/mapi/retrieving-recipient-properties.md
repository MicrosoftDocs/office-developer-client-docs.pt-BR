---
title: Recuperar as propriedades de destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770254"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="75872-103">Recuperar as propriedades de destinatário</span><span class="sxs-lookup"><span data-stu-id="75872-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="75872-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75872-104">**Applies to**: Outlook</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="75872-105">Para acessar uma ou mais propriedades de uma entrada de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="75872-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="75872-106">Para cada entrada do catálogo de endereços de interesse, chame [IAddrBook::OpenEntry](iaddrbook-openentry.md), passando o identificador de entrada do destino da lista de distribuição ou de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="75872-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="75872-107">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="75872-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="75872-108">Chame o usuário de mensagens ou um método de [IMAPIProp::GetProps](imapiprop-getprops.md) da lista de distribuição para cada entrada do catálogo de endereços de interesse, com uma lista das propriedades para recuperar um ou mais.</span><span class="sxs-lookup"><span data-stu-id="75872-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="75872-109">Chame [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passando uma estrutura [ADRLIST](adrlist.md) que contém todas as propriedades para todas as entradas do catálogo de endereço desejado.</span><span class="sxs-lookup"><span data-stu-id="75872-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="75872-110">Como uma chamada de **PrepareRecips** pode retornar informações de endereço de várias entradas do catálogo, é a estratégia preferível quando você está interessado em mais de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="75872-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

