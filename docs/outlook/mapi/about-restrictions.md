---
title: Sobre as restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d7294527fcd557ae2d4824b9a3215ff464f62c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766099"
---
# <a name="about-restrictions"></a>Sobre as restrições

  
  
**Aplica-se a**: Outlook 
  
Uma restrição é uma maneira para limitar o número de linhas em um modo de exibição somente as linhas com valores de colunas que correspondem a critérios específicos. Há muitas oportunidades diferentes para o uso de restrições com tabelas. Aplicativos cliente podem usar a restrições, por exemplo, para filtrar uma tabela de conteúdo para mensagens enviadas por uma pessoa específica, para pesquisar por linhas que não oferecem suporte a uma propriedade ou tem definido uma propriedade para um valor específico ou para procurar por destinatários duplicados dentro um Mensagem. 
  
Os métodos [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: FindRow](imapitable-findrow.md) são usados para definir restrições em uma tabela. **Restrict** aplica a restrição à tabela sem recuperar qualquer linha. Para recuperar apenas aquelas que atendam a restrição de linhas, uma chamada subsequente para [IMAPITable:: QueryRows](imapitable-queryrows.md) ou um método semelhante é necessária. **FindRow** aplica a restrição e recupera a primeira linha da tabela que corresponde aos critérios. **FindRow** aplica uma restrição temporária, que está no existência apenas para a duração da chamada, enquanto **Restrict** aplica uma restrição mais permanente. 
  
Alguns clientes podem construir uma restrição usando colunas não na coluna atual definidas. Suporte de tal uma restrição é opcional e implementadores de tabela que dão suporte ao agregam valor, particularmente para tabelas de conteúdo. Implementadores de tabela que não têm suporte podem retornar o valor MAPI_E_TOO_COMPLEX de uma chamada **Restrict** ou o valor de E_NOT_FOUND de uma chamada **FindRow** . 
  
Os clientes devem estar cientes de que, mesmo se o provedor oferece suporte a restrições em colunas não no conjunto coluna atual, elas receberão um melhor desempenho geral, especificando as colunas que pretendem usar em suas restrições com [IMAPITable::SetColumns](imapitable-setcolumns.md) .
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

