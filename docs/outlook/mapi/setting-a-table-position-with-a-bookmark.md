---
title: Definir uma posição de tabela com um indicador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351230"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Definir uma posição de tabela com um indicador

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um indicador é um recurso que indica um local específico em uma tabela. Definir um indicador torna possível retornar a uma posição mais tarde, um recurso que pode melhorar significativamente o desempenho das operações da tabela. MAPI define três indicadores padrão: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Aponta para a linha atual em uma tabela.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Aponta para a primeira linha em uma tabela.  <br/> |
|BOOKMARK_END  <br/> |Aponta para a última linha em uma tabela.  <br/> |
   
Os implementadores de tabela são necessários para dar suporte a esses indicadores padrão e também podem oferecer suporte a outros. No enTanto, como os indicadores são recursos e recursos são limitados, os usuários indicadores devem liberá-los o mais rápido possível. 
  
 **Para definir um indicador na posição da tabela atual**
  
- Call [IMAPITable:: CreateBookmark](imapitable-createbookmark.md). Ocasionalmente, não haverá memória suficiente disponível para alocar o novo indicador, **** fazendo com que CreateBookmark retorne o valor de erro MAPI_E_UNABLE_TO_COMPLETE. 
    
 **Para liberar um indicador**
  
- Call [IMAPITable:: FreeBookmark](imapitable-freebookmark.md).
    
 **Para mover o cursor para uma posição com indicador**
  
- Call [IMAPITable:: SeekRow](imapitable-seekrow.md). **SeekRow** estabelece um novo valor para a posição BOOKMARK_CURRENT. **SeekRow** pode ser usado, por exemplo, para posicionar uma tabela de dez linhas a partir da posição atual ou para começar no início. Os clientes ou provedores de serviço podem buscar o atual, o início ou o fim de uma tabela ou qualquer outra posição associada a um indicador predefinido. Eles podem ser movidos para uma direção para frente ou para trás e limitar a operação a um número especificado de linhas. Como regra, os chamadores devem procurar por até 50 linhas com o **SeekRow**; [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) deve ser usado com números maiores de linhas. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

