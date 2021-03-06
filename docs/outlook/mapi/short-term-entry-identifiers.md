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
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439559"
---
# <a name="short-term-entry-identifiers"></a>Identificadores de entradas de curto prazo

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um identificador de entrada de curto prazo é atribuído por um provedor de serviços a um objeto quando o identificador deve ser construído rapidamente e não precisa durar ao longo do tempo ou da distância. A exclusividade de um identificador de entrada de curto prazo é garantida apenas durante a vida útil da sessão atual na estação de trabalho atual. Normalmente, um identificador de entrada de curto prazo só é válido até que o objeto que ele representa seja liberado. 
  
Identificadores de entrada de curto prazo são atribuídos a linhas em tabelas e entradas em caixas de diálogo, onde é necessário fornecer dados rapidamente para navegação. Por exemplo, os provedores de armazenamento de mensagens atribuem identificadores de entrada de curto prazo a linhas de mensagens em uma tabela de conteúdo e a destinatários em uma tabela de destinatários. 

Os clientes podem usar esses identificadores de entrada de curto prazo para abrir os objetos representados pelas linhas da tabela. No entanto, ao contrário dos identificadores de entrada de longo prazo que podem ser usados com qualquer um dos métodos **OpenEntry,** identificadores de entrada de curto prazo devem ser usados com o método **OpenEntry** do contêiner. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementando identificadores de entrada de curto prazo

As maneiras mais comuns de implementar identificadores de entrada de curto prazo incluem o seguinte:
  
- Tornar os identificadores de entrada de curto prazo iguais aos identificadores de longo prazo, deixando todos os sinalizadores sem sinalização. 
    
- Tornando os identificadores de entrada de curto prazo diferentes dos identificadores de longo prazo, definindo todos os sinalizadores. 
    
Os clientes podem identificar um identificador de entrada de curto prazo do segundo tipo examinando seu membro **abFlags** da seguinte forma: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Alguns provedores de serviços limpam um ou mais sinalizadores para criar identificadores de entrada de curto prazo com maior validade. Por exemplo, os seguintes **membros abFlags** representam identificadores de entrada de curto prazo que podem ser usados por vários dias ou para várias sessões: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Os clientes adquirem, usam e descartam rapidamente identificadores de entrada de curto prazo. Em grande parte, eles podem ser usados da mesma maneira que identificadores de entrada de longo prazo. Eles podem ser recuperados de uma tabela, passados para o **método OpenEntry** e comparados com o **método CompareEntryIDs.** A única exceção é que eles nunca são retornados do [método IMAPIProp::GetProps.](imapiprop-getprops.md) As propriedades retornadas de **GetProps** são sempre identificadores de entrada de longo prazo. 
  
## <a name="see-also"></a>Confira também

- [Identificadores de entrada MAPI](mapi-entry-identifiers.md)

