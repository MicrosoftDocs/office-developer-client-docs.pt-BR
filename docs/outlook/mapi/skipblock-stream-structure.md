---
title: Estrutura de fluxo de SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d84704300602bada4cf93c9d3f6622feaf16f352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770431"
---
# <a name="skipblock-stream-structure"></a>Estrutura de fluxo de SkipBlock

  
  
**Aplica-se a**: Outlook 
  
Uma estrutura de fluxo de SkipBlock é um bloco de dados que começa com um número inteiro que especifica o tamanho da parte restante do bloco. Essa estrutura stream existe em um stream [FieldDefinition](fielddefinition-stream-structure.md) se a definição de campo está no formato PropDefV2. 
  
A finalidade de uma estrutura de fluxo de SkipBlock depende de seu local relativo em uma série de como estruturas no elemento SkipBlocks dados de um stream FieldDefinition. A série de SkipBlocks deve conter pelo menos uma estrutura SkipBlock que finaliza a série e tem o elemento de dados de tamanho igual a 0. Se a primeira estrutura não é a estrutura de encerramento (ou seja, o elemento de dados de tamanho é maior que 0), Outlook pressupõe que a primeira estrutura Especifica o nome do campo em Unicode (UTF-16).
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem especificada abaixo.
  
- Tamanho: DWORD (4 bytes), o tamanho, em número de bytes, do elemento de dados de conteúdo.
    
- Conteúdo: Uma matriz de bytes. A contagem dessa matriz é igual do elemento de dados de tamanho. O significado do elemento de dados de conteúdo depende do local da estrutura SkipBlock na série e a versão do Outlook. Se a primeira estrutura de SkipBlock não for a estrutura de encerramento, o Outlook considera a estrutura de SkipBlock primeira como a estrutura de fluxo de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica o nome do campo em Unicode. 
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo de FieldDefinition](fielddefinition-stream-structure.md)
  
[Estrutura de fluxo de FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

