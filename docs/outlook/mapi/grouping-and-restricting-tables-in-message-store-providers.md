---
title: Agrupar e restringir tabelas em provedores do repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766664"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Agrupar e restringir tabelas em provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 
  
Aplicativos de cliente com frequência permitem aos usuários algum controle sobre como o conteúdo de uma pasta é exibido. Normalmente, um usuário pode optar por mensagens agrupados de acordo com o valor de uma ou mais propriedades de mensagem, ou pode optar por excluir mensagens que correspondem a determinados critérios. Isso é feito usando o [IMAPITable: IUnknown](imapitableiunknown.md) interface. Aplicativos cliente podem restringir as linhas retornadas da tabela para todos os critérios que o usuário especifica. Portanto, uma mensagem armazene as necessidades do provedor para implementar os seguintes métodos **IMAPITable** . 
  
|IMAPITable * * método * *|**Descrição**|
|:-----|:-----|
|[IMAPITable::ExpandRow](imapitable-findrow.md) <br/> |Retorna a tabela linhas que coincidem com os critérios especificados.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Retorna o conjunto de colunas em uma tabela ou o conjunto de colunas atualmente em uso.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Retorna uma ou mais linhas de uma tabela, iniciando a partir de uma determinada posição.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Aplica uma restrição a uma tabela para que as chamadas subsequentes **FindRow** retornam somente as linhas que coincidem com a restrição.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Especifica quais colunas devem ser retornadas quando linhas são recuperadas da tabela.  <br/> |
   
Restrições podem ser complexas para implementar; Para obter mais informações, consulte [Sobre restrições](about-restrictions.md). Para obter mais informações sobre como implementar as tabelas, consulte [As tabelas de MAPI](mapi-tables.md).
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

