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
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316041"
---
# <a name="setting-a-table-position-with-a-filter"></a>Definir uma posição de tabela com um filtro

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Tabela os usuários podem mover o cursor para uma linha que coincida com um conjunto de critérios de filtro. Os filtros podem ser baseados em uma variedade de diretrizes, como valores de propriedade de coluna, bitmasks ou subobjetos. Os filtros são especificados em MAPI usando uma estrutura [SRestriction](srestriction.md) . 
  
 **Para posicionar uma tabela na primeira linha que corresponda aos critérios estabelecidos em uma restrição**
  
- Chame o método imApitable [:: FindRow](imapitable-findrow.md) . Começando com a linha representada por um indicador específico, o **FindRow** pesquisa em uma direção para a frente ou para trás para localizar uma linha que corresponda aos critérios especificados na restrição. O **FindRow** pode ser útil para implementar uma barra de rolagem baseada em cadeias de caracteres, em vez de valores fracionários. Por exemplo, um cliente pode chamar a implementação do **FindRow** de MAPI ao pesquisar o catálogo de endereços integrados para habilitar um usuário, inserindo um ou mais caracteres, para localizar o primeiro nome que começa com os caracteres especificados. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

