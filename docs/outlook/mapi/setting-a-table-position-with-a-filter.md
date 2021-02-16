---
title: Definindo uma posição de tabela com um filtro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425467"
---
# <a name="setting-a-table-position-with-a-filter"></a>Definindo uma posição de tabela com um filtro

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os usuários da tabela podem mover o cursor para uma linha que corresponde a um conjunto de critérios de filtro. Os filtros podem ser baseados em uma variedade de diretrizes, como valores de propriedade de coluna, bitmasks ou subobjetos. Os filtros são especificados em MAPI usando [uma estrutura SRestriction.](srestriction.md) 
  
 **Para posicionar uma tabela na primeira linha que corresponde aos critérios estabelecidos em uma restrição**
  
- Chame o [método IMAPITable::FindRow.](imapitable-findrow.md) Começando com a linha representada por um indicador específico, **FindRow** pesquisa em uma direção para frente ou para trás para localizar uma linha que corresponde aos critérios especificados na restrição. **FindRow** pode ser útil para implementar uma barra de rolagem baseada em cadeias de caracteres, em vez de valores fracionais. Por exemplo, um cliente pode chamar a implementação de **FindRow** de MAPI ao pesquisar o livro de endereços integrado para habilitar um usuário, inserindo um ou mais caracteres, para localizar o primeiro nome que começa com os caracteres especificados. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

