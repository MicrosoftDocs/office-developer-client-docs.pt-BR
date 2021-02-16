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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426671"
---
# <a name="retrieving-recipient-properties"></a>Recuperar propriedades de destinatários
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Para acessar uma ou mais propriedades de uma entrada de agenda
  
1. Para cada entrada de interesse do livro de endereços, chame [IAddrBook::OpenEntry](iaddrbook-openentry.md), passando o identificador de entrada do usuário de mensagens de destino ou lista de distribuição.
    
2. Em seguida, faça um dos seguintes:
    
   - Chame o usuário de mensagens ou o método [IMAPIProp::GetProps](imapiprop-getprops.md) da lista de mensagens para cada entrada de interesse do livro de endereços, com uma lista de uma ou mais propriedades a recuperar. 
    
   - Chame [IAddrBook::P repareRecips](iaddrbook-preparerecips.md), passando uma estrutura [ADRLIST](adrlist.md) que contém todas as propriedades para todas as entradas do livro de endereços desejado. Como uma chamada para **PrepareRecips** pode retornar informações para várias entradas do livro de endereços, essa é a estratégia preferível quando você está interessado em mais de um destinatário. 
    

