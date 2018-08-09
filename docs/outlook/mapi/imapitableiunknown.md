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
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767344"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Fornece uma exibição somente leitura de uma tabela. **IMAPITable** é usado por clientes e provedores de serviços para manipular a maneira como uma tabela é exibida. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos Table  <br/> |
|Implementada por:  <br/> |Provedores de serviços e MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos clientes, provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPITable  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) contendo informações sobre o erro anterior na tabela.  <br/> |
|[Aviso](imapitable-advise.md) <br/> |Registra para receber notificações de eventos especificados que afetam a tabela.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Cancela o envio de notificações configuradas anteriormente com uma chamada ao método **IMAPITable::Advise** .  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Retorna o status e o tipo da tabela.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Define as propriedades específicas e a ordem das propriedades aparecer como colunas na tabela.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Retorna uma lista das colunas da tabela.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Retorna o número total de linhas na tabela.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Move o cursor para uma posição específica na tabela.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Move o cursor para uma posição fracional aproximada na tabela.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Recupera a posição da linha de tabela atual do cursor, com base em um valor fracionário.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Localiza a próxima linha em uma tabela que corresponde a determinados critérios de pesquisa.  <br/> |
|[Restringir](imapitable-restrict.md) <br/> |Aplica um filtro a uma tabela, reduzindo a linha definida como apenas as linhas que correspondem aos critérios especificados.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marca a posição atual da tabela.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libera a memória associada a um indicador.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Ordena as linhas da tabela com base nos critérios de classificação.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Recupera a ordem de classificação atual para uma tabela.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Retorna uma ou mais linhas de uma tabela, começando à meia posição atual do cursor.  <br/> |
|[Abort](imapitable-abort.md) <br/> |Interrompe a qualquer operação assíncrona em andamento atualmente para a tabela.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Expande uma categoria de tabela recolhida, adicionando as linhas da folha que pertencem à categoria para o modo de exibição de tabela.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Recolhe uma categoria de tabela expandida, removendo as linhas da folha que pertencem à categoria da visualização de tabela.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspende o processamento até que um ou mais operações assíncronas em andamento na tabela forem concluídas.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Retorna os dados necessários para recriar as atuais recolhido ou expandido o estado de uma tabela categorizado.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Recriará o estado atual de expandidos ou recolhido de uma tabela categorizado usando os dados que foi salvo por uma chamada anterior para o método **IMAPITable::GetCollapseState** .  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

