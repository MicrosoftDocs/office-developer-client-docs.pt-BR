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
# <a name="deleting-a-recipient"></a>Excluir um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para remover um ou mais entradas do catálogo de endereços de um contêiner modificável**
  
- Chame o método [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , passando uma matriz de identificadores de entrada que representam as entradas do catálogo de endereços a ser excluído. **DeleteEntries** pode retornar um aviso, MAPI_W_PARTIAL_COMPLETION, para indicar que ele não foi possível excluir uma ou mais das entradas. Testar esse valor de retorno à macro **HR_FAILED** e chame o método de [IMAPIProp::GetLastError](imapiprop-getlasterror.md) do contêiner se forem necessárias mais informações sobre o problema. 
    
Quando você mantiver um ponteiro à estrutura [ADRENTRY](adrentry.md) de uma entrada excluído em seu cache, você ainda poderá recuperar as propriedades utilizando seu identificador de entrada. Isso ocorre porque a entrada só é marcada para exclusão. MAPI mantém um nível de acesso a essas entradas marcadas por design. 
  

