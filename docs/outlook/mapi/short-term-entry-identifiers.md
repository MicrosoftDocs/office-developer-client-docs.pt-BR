---
title: Identificadores de entradas de curto prazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 03352b55589138d406ad3e4ee0756fc44bca8c78
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580611"
---
# <a name="short-term-entry-identifiers"></a>Identificadores de entradas de curto prazo

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um identificador de entrada de curto prazo é atribuído por um provedor de serviço a um objeto quando o identificador deve ser construído rapidamente e não precisa dure sobre tempo ou distância. A exclusividade de um identificador de entrada de curto prazo é garantida somente durante a vigência da sessão atual na estação de trabalho atual. Normalmente, um identificador de entrada de curto prazo é válido somente até que o objeto que ele representa for lançado. 
  
Identificadores de entrada de curto prazo são atribuídos às linhas em tabelas e às entradas nas caixas de diálogo, onde é necessário fornecer dados rapidamente para navegação. Por exemplo, provedores de armazenamento de mensagem atribuir identificadores de entrada de curto prazo às linhas de mensagens em uma tabela de conteúdo e para destinatários em uma tabela de destinatários. 

Clientes podem usar esses identificadores de entrada de curto prazo para abrir os objetos representados por linhas da tabela. No entanto, ao contrário de longo prazo identificadores de entrada que podem ser usados com qualquer um dos métodos **OpenEntry** , a curto prazo identificadores de entrada devem ser usados com o método de **OpenEntry** do contêiner. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementando a curto prazo identificadores de entrada

Maneiras de implementar a curto prazo identificadores de entrada mais comuns incluem o seguinte:
  
- Os identificadores de entrada de curto prazo fazendo o mesmo que os identificadores de longo prazo, deixando todos os sinalizadores não definidas. 
    
- Tornando os identificadores de entrada de curto prazo diferente dos identificadores de longo prazo, a definição de todos os sinalizadores. 
    
Os clientes podem identificar um identificador de entrada de curto prazo do segundo tipo examinando sua lista de membros **abFlags** da seguinte maneira: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Alguns provedores de serviços desmarque um ou mais sinalizadores para criar a curto prazo identificadores de entrada que têm validade maior. Por exemplo, os seguintes membros **abFlags** representam a curto prazo identificadores de entrada que podem ser usados para vários dias ou para várias sessões: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Clientes rapidamente adquirem, usam e descartar os identificadores de entrada de curto prazo. Na maioria das vezes, pode ser usados da mesma maneira como os identificadores de entrada de longo prazo. Eles podem ser recuperados de uma tabela, passadas para o método **OpenEntry** e comparado com o método **CompareEntryIDs** . A única exceção é que nunca são retornadas pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) . As propriedades retornadas de **GetProps** são sempre identificadores de entrada de longo prazo. 
  
## <a name="see-also"></a>Confira também

- [Identificadores de entrada MAPI](mapi-entry-identifiers.md)

