---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420112"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece uma exibição somente leitura de uma tabela. **IMAPITable** é usado por clientes e provedores de serviços para manipular a maneira como uma tabela é exibida. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Objetos Table  <br/> |
|Implementado por:  <br/> |Provedores de serviços e MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente, provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPITable  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior na tabela.  <br/> |
|[Advise](imapitable-advise.md) <br/> |Registra para receber notificação de eventos especificados que afetam a tabela.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Cancela o envio de notificações configuradas anteriormente com uma chamada para o **método IMAPITable::Advise.**  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Retorna o status e o tipo da tabela.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Define as propriedades específicas e a ordem das propriedades que aparecerão como colunas na tabela.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Retorna uma lista de colunas para a tabela.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Retorna o número total de linhas na tabela.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Move o cursor para uma posição específica na tabela.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Move o cursor para uma posição fracionada aproximada na tabela.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Recupera a posição atual da linha da tabela do cursor, com base em um valor fracionado.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Localiza a próxima linha em uma tabela que corresponde a critérios de pesquisa específicos.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Aplica um filtro a uma tabela, reduzindo o conjunto de linhas apenas para as linhas que corresponderem aos critérios especificados.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marca a posição atual da tabela.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libera a memória associada a um indicador.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Ordena as linhas da tabela com base em critérios de classificação.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Recupera a ordem de classificação atual para uma tabela.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Retorna uma ou mais linhas de uma tabela, começando na posição atual do cursor.  <br/> |
|Anular** <br/> |Interrompe qualquer operação assíncrona em andamento para a tabela.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Expande uma categoria de tabela recolhido, adicionando as linhas folha pertencentes à categoria ao exibição de tabela.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspende o processamento até que uma ou mais operações assíncronas em andamento na tabela tenham sido concluídas.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Retorna os dados necessários para recriar o estado recolhido ou expandido atual de uma tabela categorizada.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Recria o estado expandido ou recolhido atual de uma tabela categorizada usando dados salvos por uma chamada anterior para o método **IMAPITable::GetCollapseState.**  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

