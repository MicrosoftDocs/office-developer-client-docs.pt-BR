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
# <a name="retrieving-recipient-properties"></a>Recuperar as propriedades de destinatário
  
**Aplica-se a**: Outlook 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Para acessar uma ou mais propriedades de uma entrada de catálogo de endereços
  
1. Para cada entrada do catálogo de endereços de interesse, chame [IAddrBook::OpenEntry](iaddrbook-openentry.md), passando o identificador de entrada do destino da lista de distribuição ou de usuário de mensagens.
    
2. Siga um destes procedimentos:
    
   - Chame o usuário de mensagens ou um método de [IMAPIProp::GetProps](imapiprop-getprops.md) da lista de distribuição para cada entrada do catálogo de endereços de interesse, com uma lista das propriedades para recuperar um ou mais. 
    
   - Chame [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passando uma estrutura [ADRLIST](adrlist.md) que contém todas as propriedades para todas as entradas do catálogo de endereço desejado. Como uma chamada de **PrepareRecips** pode retornar informações de endereço de várias entradas do catálogo, é a estratégia preferível quando você está interessado em mais de um destinatário. 
    

