---
title: Recuperando dados de linhas de tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405251"
---
# <a name="retrieving-data-from-table-rows"></a>Recuperando dados de linhas de tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recuperar linhas de uma tabela envolve:
  
- Obtendo os valores de propriedade para todas as colunas.
    
- Modificando a posição atual.
    
Uma das colunas necessárias na maioria das tabelas é um identificador de entrada — a propriedade PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) — que pode ser usada para abrir o objeto que representa **a** linha. Esse identificador de entrada geralmente é um identificador de entrada de curto prazo, que não persiste após o tempo de vida da tabela. No entanto, ele pode ser um identificador de longo prazo se o provedor de serviços que implementa a tabela suporta apenas um tipo de identificador de entrada.
  
Os clientes e provedores de serviços podem fazer uma das seguintes chamadas para recuperar linhas:
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Recupera um número especificado de linhas começando com a linha atual em uma direção para frente ou para trás.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Recupera todas as linhas em uma tabela.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera uma linha em uma tabela de acordo com o valor de sua coluna de índice. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) geralmente é a coluna de índice de uma tabela.  <br/> |
   
Quando uma propriedade opcional é incluída como uma das colunas em uma tabela, algumas das linhas podem ter valores válidos para a coluna, enquanto outras podem não ter. Se existe um valor válido para uma coluna depende se o objeto que fornece as informações para a linha define a propriedade. Dependendo da implementação do objeto, uma propriedade inexistente pode ser representada na tabela como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou um valor arbitrário. Os usuários de tabelas devem ter cuidado para diferenciar entre propriedades que não são inexistentes e têm valores e propriedades sem sentido que existem e têm valores válidos. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

