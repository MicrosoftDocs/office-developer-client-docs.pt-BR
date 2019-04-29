---
title: Agrupar e restringir tabelas em provedores de repositórios de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428981"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Agrupar e restringir tabelas em provedores de repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente freqüentemente permitem que os usuários tenham controle sobre como o conteúdo de uma pasta é exibido. Normalmente, um usuário pode optar por ter mensagens agrupadas de acordo com o valor de uma ou mais propriedades de mensagem, ou pode optar por excluir mensagens que correspondam a determinados critérios. Isso é feito usando a interface [IMAPITable: IUnknown](imapitableiunknown.md) . Os aplicativos cliente podem restringir as linhas retornadas da tabela para qualquer critério especificado pelo usuário. Portanto, um provedor de repositório de mensagens precisa implementar os **** métodos IMAPITable a seguir. 
  
|ImApitable * * método * *|**Descrição**|
|:-----|:-----|
|[IMAPITable::ExpandRow](imapitable-findrow.md) <br/> |Retorna linhas de tabela que correspondem aos critérios especificados.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Retorna o conjunto de colunas em uma tabela ou o conjunto de colunas usadas no momento.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Retorna uma ou mais linhas de uma tabela, começando a partir de uma determinada posição.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Aplica uma restrição a uma tabela para que chamadas subsequentes para o **FindRow** retornem somente as linhas que correspondem à restrição.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Especifica quais colunas devem ser retornadas quando as linhas são recuperadas da tabela.  <br/> |
   
As restrições podem ser complexas para implementar; para obter mais informações, consulte [about Restrictions](about-restrictions.md). Para obter mais informações sobre a implementação de tabelas, consulte [tabelas MAPI](mapi-tables.md).
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

