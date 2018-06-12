---
title: Recuperando dados de linhas da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770263"
---
# <a name="retrieving-data-from-table-rows"></a>Recuperando dados de linhas da tabela

  
  
**Aplica-se a**: Outlook 
  
Recuperação de linhas de uma tabela envolve:
  
- Obtendo os valores de propriedade para todas as colunas.
    
- Modificando a posição atual.
    
Uma das colunas necessárias na maioria das tabelas é um identificador de entrada — a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) — que pode ser usado para abrir o objeto que representa a linha. Geralmente, esse identificador de entrada é um identificador curto prazo de entrada, que não persiste passou a vida útil da tabela. No entanto, ele pode ser um identificador de longo prazo, se o provedor de serviço implementando a tabela só oferece suporte a um tipo de identificador de entrada.
  
Clientes e provedores de serviços podem fazer uma das seguintes chamadas para recuperar linhas:
  
|||
|:-----|:-----|
|[IMAPITable:: QueryRows](imapitable-queryrows.md) <br/> |Recupera um número especificado de linhas, começando com a linha atual na direção frente ou para trás.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Recupera todas as linhas em uma tabela.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera uma linha em uma tabela de acordo com o valor da coluna seu índice. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é geralmente a coluna de índice para uma tabela.  <br/> |
   
Quando uma propriedade opcional é incluída como uma das colunas em uma tabela, algumas das linhas podem ter os valores válidos para a coluna, enquanto outros usuários talvez não. Se um valor válido existe para uma coluna depende se o objeto fornecendo as informações para a linha define a propriedade. Dependendo da implementação do objeto, uma propriedade inexistentes pode ser representada na tabela como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou um valor arbitrário. Os usuários das tabelas devem tomar cuidadosos diferenciar entre as propriedades que são inexistente e têm valores insignificante e que existem e têm valores válidos. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

