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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326205"
---
# <a name="opening-a-view-descriptor"></a>Abrir um descritor de modo de exibição
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitas pastas podem ser abertas com um modo de exibição normal, um modo de exibição padrão ou qualquer número de exibições personalizadas. Um modo de exibição descreve como exibir o conteúdo de uma pasta. O modo de exibição normal é usado quando não há um modo de exibição alternativo e quando você está abrindo a pasta pela primeira vez. Quando um modo de exibição alternativo existe, você deve usá-lo para abrir a pasta.
  
Um modo de exibição é descrito em uma mensagem conhecida como um descritor de modo de exibição. Os descritores de modo geralmente são criados como mensagens associadas e podem aparecer nas pastas de exibição comum ou pessoal ou em qualquer pasta IPM.
  
### <a name="to-open-a-view-descriptor"></a>Para abrir um descritor de modo de exibição
  
1. Chame [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable para recuperar a tabela de conteúdo associada da pasta. 
    
2. Criar uma restrição que localiza somente mensagens com a classe de mensagem reservada para exibir descritores e Call [IMAPITable:: Restrict](imapitable-restrict.md) para limitar a tabela e IMAPITable [:: QueryRows](imapitable-queryrows.md) para recuperar as linhas apropriadas ou...
    
   Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps da pasta para recuperar sua propriedade **PR_DEFAULT_VIEW_ENTRYID** ([pidtagdefaultviewentryid Canonical](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** contém o identificador de entrada para a mensagem que contém o descritor de modo de exibição padrão de uma pasta. Essa chamada será bem-sucedida se a pasta suportar o uso do sinalizador MAPI_ASSOCIATED em chamadas para [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) e [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontenttable.
    
3. Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) com o identificador de entrada do descritor de modo de exibição para abri-lo. 
    

