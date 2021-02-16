---
title: Sobre restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433105"
---
# <a name="about-restrictions"></a>Sobre restrições

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma restrição é uma maneira de limitar o número de linhas em um modo de exibição apenas às linhas com valores para colunas que corresponderem a critérios específicos. Há muitas oportunidades diferentes para o uso de restrições com tabelas. Aplicativos cliente podem usar restrições, por exemplo, para filtrar uma tabela de conteúdo para mensagens enviadas por uma determinada pessoa, para pesquisar linhas que não suportam uma propriedade ou definir uma propriedade com um valor específico ou para procurar destinatários duplicados dentro de uma mensagem. 
  
Os [métodos IMAPITable::Restrict](imapitable-restrict.md) e [IMAPITable::FindRow](imapitable-findrow.md) são usados para definir restrições em uma tabela. **Restringir** aplica a restrição à tabela sem recuperar nenhuma linha. Para recuperar somente as linhas que atendem à restrição, é necessária uma chamada subsequente para [IMAPITable::QueryRows](imapitable-queryrows.md) ou um método semelhante. **FindRow** aplica a restrição e recupera a primeira linha na tabela que corresponde aos critérios. **FindRow** aplica uma restrição temporária, que existe apenas pela duração da chamada, enquanto **Restrict** aplica uma restrição mais permanente. 
  
Alguns clientes podem criar uma restrição usando colunas que não estão no conjunto de colunas atual. O suporte a essa restrição é opcional e os implementadores de tabela que a suportam agregam valor, especialmente para tabelas de conteúdo. Implementadores de tabela que não a suportam podem retornar o valor MAPI_E_TOO_COMPLEX de uma **chamada** Restringir ou o valor MAPI_E_NOT_FOUND de uma **chamada FindRow.** 
  
Os clientes devem estar cientes de que, mesmo que o provedor tenha restrições de suporte em colunas que não estão no conjunto de colunas atual, eles obterão melhor desempenho geral especificando as colunas que pretendem usar em suas restrições com [IMAPITable::SetColumns](imapitable-setcolumns.md).
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

