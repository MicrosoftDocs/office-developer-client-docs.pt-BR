---
title: Definindo uma posição de tabela com um indicador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422457"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Definindo uma posição de tabela com um indicador

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um indicador é um recurso que indica um local específico em uma tabela. A definição de um indicador possibilita retornar a uma posição posteriormente, um recurso que pode melhorar significativamente o desempenho das operações de tabela. O MAPI define três indicadores padrão: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Aponta para a linha atual em uma tabela.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Aponta para a primeira linha em uma tabela.  <br/> |
|BOOKMARK_END  <br/> |Aponta para a última linha em uma tabela.  <br/> |
   
Implementadores de tabela são necessários para dar suporte a esses indicadores padrão e também podem dar suporte a outros. No entanto, como os indicadores são recursos e recursos são limitados, os usuários de indicadores devem libera-los assim que possível. 
  
 **Para definir um indicador na posição atual da tabela**
  
- Chame [IMAPITable::CreateBookmark](imapitable-createbookmark.md). Ocasionalmente, haverá memória insuficiente disponível para alocar o novo indicador, fazendo com que **CreateBookmark** retorne o valor MAPI_E_UNABLE_TO_COMPLETE erro. 
    
 **Para liberar um indicador**
  
- Chame [IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Para mover o cursor para uma posição com indicador**
  
- Chame [IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** estabelece um novo valor para a BOOKMARK_CURRENT atual. **SeekRow** pode ser usado, por exemplo, para posicionar uma tabela a dez linhas a partir da posição atual ou para começar de novo no início. Os clientes ou provedores de serviços podem procurar o atual, o início ou o final de uma tabela ou qualquer outra posição associada a um indicador predefinido. Eles podem se mover em direção à frente ou para trás e limitar a operação a um número especificado de linhas. Como regra, os chamadores devem procurar por no máximo 50 linhas com **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) deve ser usado com um número maior de linhas. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

