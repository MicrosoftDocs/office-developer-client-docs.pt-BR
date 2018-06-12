---
title: Abrindo um descritor de modo de exibição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 525c817cfc3bdcf96455d35025e85486ec8b5b42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768174"
---
# <a name="opening-a-view-descriptor"></a>Abrindo um descritor de modo de exibição
  
**Aplica-se a**: Outlook 
  
Muitas pastas podem ser abertas com um modo de exibição normal, um modo de exibição padrão ou qualquer número de exibições personalizadas. Um modo de exibição descreve como exibir o conteúdo de uma pasta. O modo de exibição normal é usado quando não há nenhum modo de exibição alternativo e quando você está abrindo a pasta pela primeira vez. Quando houver um modo de exibição alternativo, você deve usá-lo para abrir a pasta.
  
Um modo de exibição é descrito em uma mensagem conhecida como descritor de modo de exibição. Descritores de modo de exibição normalmente são criadas como mensagens associadas e podem aparecer nas pastas de exibição comuns ou pessoal ou em qualquer pasta IPM.
  
### <a name="to-open-a-view-descriptor"></a>Para abrir um descritor de modo de exibição
  
1. Chame [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para recuperar a tabela de conteúdo associado para a pasta. 
    
2. Criar uma restrição que localiza somente as mensagens com a classe de mensagem reservada para descritores de modo de exibição e chamar [IMAPITable:: Restrict](imapitable-restrict.md) para limitar a tabela e [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar as linhas apropriadas, ou …
    
   Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da pasta para recuperar sua propriedade **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** contém o identificador de entrada para a mensagem contendo o descritor de modo de exibição padrão para uma pasta. Essa chamada será bem-sucedida se a pasta dá suporte ao uso do sinalizador MAPI_ASSOCIATED em chamadas [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) com o identificador de entrada do descritor de modo de exibição para abri-lo. 
    

