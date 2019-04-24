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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328655"
---
# <a name="retrieving-data-from-table-rows"></a>Recuperando dados de linhas de tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A recuperação de linhas de uma tabela envolve:
  
- Obter os valores de propriedade para todas as colunas.
    
- Modificar a posição atual.
    
Uma das colunas obrigatórias na maioria das tabelas é um identificador de entrada, a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), que pode ser usada para abrir o objeto que representa a linha. Normalmente, esse identificador de entrada é um identificador de entrada de curto prazo, que não é mantido após o tempo de vida da tabela. No enTanto, pode ser um identificador de longo prazo se o provedor de serviços que está implementando a tabela suportar apenas um tipo de identificador de entrada.
  
Os clientes e provedores de serviços podem fazer uma das seguintes chamadas para recuperar linhas:
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Recupera um número especificado de linhas começando com a linha atual em uma direção para frente ou para trás.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Recupera todas as linhas em uma tabela.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera uma linha em uma tabela de acordo com o valor de sua coluna de índice. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) geralmente é a coluna de índice para uma tabela.  <br/> |
   
Quando uma propriedade opcional é incluída como uma das colunas em uma tabela, algumas das linhas podem ter valores válidos para a coluna, enquanto outras não. Se um valor válido existe para uma coluna depende se o objeto que fornece as informações para a linha define a propriedade. Dependendo da implementação do objeto, uma propriedade não existente pode ser representada na tabela como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou um valor arbitrário. Os usuários das tabelas devem ter cuidado para diferenciar as propriedades não existentes e ter valores e propriedades insignificantes que existem e que têm valores válidos. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

