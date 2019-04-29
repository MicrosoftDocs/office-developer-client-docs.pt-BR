---
title: Excluir um destinatário
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
# <a name="deleting-a-recipient"></a>Excluir um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para remover uma ou mais entradas do catálogo de endereços de um contêiner modificável**
  
- Chame o método [IABContainer::D eleteentries](iabcontainer-deleteentries.md) , passando uma matriz de identificadores de entrada que representam as entradas do catálogo de endereços a serem excluídas. **DeleteEntries** pode retornar um aviso, MAPI_W_PARTIAL_COMPLETION, para indicar que não foi possível excluir uma ou mais das entradas. Teste para esse valor de retorno com a macro **HR_FAILED** e chame o método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) do contêiner se mais informações sobre o problema forem necessárias. 
    
Quando você mantiver um ponteiro para uma estrutura [ADRENTRY](adrentry.md) de uma entrada excluída no seu cache, você ainda poderá recuperar as propriedades usando seu identificador de entrada. Isso ocorre porque a entrada só é marcada para exclusão. O MAPI mantém um nível de acesso a essas entradas marcadas por design. 
  

