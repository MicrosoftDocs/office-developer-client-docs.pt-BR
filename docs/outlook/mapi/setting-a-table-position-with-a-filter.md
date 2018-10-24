---
title: Definir uma posição de tabela com um filtro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565589"
---
# <a name="setting-a-table-position-with-a-filter"></a>Definir uma posição de tabela com um filtro

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os usuários da tabela podem mover o cursor para uma linha que corresponde a um conjunto de critérios de filtro. Filtros podem ser baseados em uma variedade de diretrizes como valores de propriedade de coluna, bitmasks ou subobjetos. Filtros são especificados em MAPI usando uma estrutura [SRestriction](srestriction.md) . 
  
 **Para posicionar uma tabela à primeira linha que corresponde aos critérios estabelecidos em uma restrição**
  
- Chame o método [IMAPITable:: FindRow](imapitable-findrow.md) . Começando com a linha representada por um determinado indicador, **FindRow** procura em uma direção frente ou para trás para localizar uma linha que corresponde aos critérios especificados na restrição. **FindRow** pode ser útil para implementar uma barra de rolagem que se baseia em cadeias de caracteres, em vez de valores fracionários. Por exemplo, um cliente pode chamar a implementação do MAPI do **FindRow** ao pesquisar o catálogo de endereços integrado para habilitar um usuário, inserindo um ou mais caracteres, para localizar o primeiro nome que começa com os caracteres especificados. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

