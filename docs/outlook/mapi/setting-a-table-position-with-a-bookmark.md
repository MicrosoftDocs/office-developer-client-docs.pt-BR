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
ms.openlocfilehash: f43e3a7e3376cb437620204a29aed9fb732d3427
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564091"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Definir uma posição de tabela com um indicador

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um indicador é um recurso que indica uma localidade específica em uma tabela. A definição de um indicador torna possível retornar para uma posição em um momento posterior, um recurso que pode melhorar significativamente o desempenho das operações de tabela. MAPI define três indicadores padrão: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Aponta para a linha atual em uma tabela.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Aponta para a primeira linha em uma tabela.  <br/> |
|BOOKMARK_END  <br/> |Aponta para a última linha em uma tabela.  <br/> |
   
Implementadores de tabela são necessárias para dar suporte a esses indicadores standard e também podem suportar a outras pessoas. No entanto, como indicadores são recursos e os recursos são limitados, os usuários do indicador devem liberá-los assim que possível. 
  
 **Para definir um indicador na posição de tabela atual**
  
- Chame [IMAPITable::CreateBookmark](imapitable-createbookmark.md). Ocasionalmente, haverá memória suficiente disponível para alocar no novo indicador, causando **CreateBookmark** retornar o valor de erro MAPI_E_UNABLE_TO_COMPLETE. 
    
 **Para liberar um indicador**
  
- Chame [IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Para mover o cursor para uma posição com indicador**
  
- Chame [IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** estabelece um novo valor para a posição de BOOKMARK_CURRENT. **SeekRow** pode ser usado, por exemplo, para posicionar um linhas da tabela dez da posição atual ou para começar novamente no início. Provedores de serviço ou clientes seek à data atual, começando, ou terminar de uma tabela ou qualquer outra posição que é associada a um indicador predefinido. Eles podem mover em um limite a operação e direção de frente ou para trás até um número especificado de linhas. Como regra, os chamadores devem buscar por meio de não mais de 50 linhas com **SeekRow**; [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) deve ser usado com um número maior de linhas. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

