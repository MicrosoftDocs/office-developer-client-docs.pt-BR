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
ms.openlocfilehash: 9a3006b43eb9f210603ff3a3d890118e7fd61d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766383"
---
# <a name="deleting-a-recipient"></a>Excluir um destinatário

  
  
**Aplica-se a**: Outlook 
  
 **Para remover um ou mais entradas do catálogo de endereços de um contêiner modificável**
  
- Chame o método [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , passando uma matriz de identificadores de entrada que representam as entradas do catálogo de endereços a ser excluído. **DeleteEntries** pode retornar um aviso, MAPI_W_PARTIAL_COMPLETION, para indicar que ele não foi possível excluir uma ou mais das entradas. Testar esse valor de retorno à macro **HR_FAILED** e chame o método de [IMAPIProp::GetLastError](imapiprop-getlasterror.md) do contêiner se forem necessárias mais informações sobre o problema. 
    
Quando você mantiver um ponteiro à estrutura [ADRENTRY](adrentry.md) de uma entrada excluído em seu cache, você ainda poderá recuperar as propriedades utilizando seu identificador de entrada. Isso ocorre porque a entrada só é marcada para exclusão. MAPI mantém um nível de acesso a essas entradas marcadas por design. 
  

