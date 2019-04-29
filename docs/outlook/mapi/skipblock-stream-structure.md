---
title: Estrutura de fluxo SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435541"
---
# <a name="skipblock-stream-structure"></a>Estrutura de fluxo SkipBlock

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma estrutura de fluxo SkipBlock é um bloco de dados que começa com um inteiro que especifica o comprimento da parte restante do bloco. Essa estrutura de fluxo existe em um fluxo de [FieldDefinition](fielddefinition-stream-structure.md) se a definição de campo estiver no formato PropDefV2. 
  
A finalidade de uma estrutura de fluxo do SkipBlock depende de seu local relativo em uma série de estruturas semelhantes no elemento de dados SkipBlocks de um fluxo de FieldDefinition. A série SkipBlocks deve conter pelo menos uma estrutura SkipBlock que termine a série e tenha o elemento de dados de tamanho igual a 0. Se a primeira estrutura não for a estrutura de terminação (ou seja, o elemento de dados size for maior que 0), o Outlook presumirá que a primeira estrutura especifica o nome do campo em Unicode (UTF-16).
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na ordem especificada abaixo.
  
- Tamanho: DWORD (4 bytes), o tamanho, em número de bytes, do elemento de dados de conteúdo.
    
- Conteúdo: uma matriz de BYTE. A contagem dessa matriz é igual ao elemento de dados de tamanho. O significado do elemento de dados de conteúdo depende do local da estrutura SkipBlock da série e da versão do Outlook. Se a primeira estrutura SkipBlock não for a estrutura de terminação, o Outlook considerará a primeira estrutura SkipBlock como a estrutura de fluxo de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica o nome do campo em Unicode. 
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo FieldDefinition](fielddefinition-stream-structure.md)
  
[Estrutura de fluxo FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

