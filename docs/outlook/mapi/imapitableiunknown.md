---
title: A imApitable IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328795"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece um modo de exibição somente leitura de uma tabela. **** IMAPITable é usado por clientes e provedores de serviço para manipular a forma como uma tabela é exibida. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos table  <br/> |
|Implementado por:  <br/> |Provedores de serviços e MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente, provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPITable  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior na tabela.  <br/> |
|[Utilizar](imapitable-advise.md) <br/> |Registra para receber notificações de eventos especificados que afetam a tabela.  <br/> |
|[Cancelar](imapitable-unadvise.md) <br/> |Cancela o envio de notificações previamente configuradas com uma chamada para o método imApitable **:: Advise** .  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Retorna o tipo e o status da tabela.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Define as propriedades específicas e a ordem das propriedades a serem exibidas como colunas na tabela.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Retorna uma lista de colunas da tabela.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Retorna o número total de linhas na tabela.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Move o cursor para uma posição específica na tabela.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Move o cursor para uma posição fracionária aproximada na tabela.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Recupera a posição de linha atual da tabela do cursor, com base em um valor fracionário.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Localiza a próxima linha em uma tabela que corresponde aos critérios de pesquisa específicos.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Aplica um filtro a uma tabela, reduzindo o conjunto de linhas somente para as linhas que correspondam aos critérios especificados.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marca a posição atual da tabela.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libera a memória associada a um indicador.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Ordena as linhas da tabela com base nos critérios de classificação.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Recupera a ordem de classificação atual para uma tabela.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Retorna uma ou mais linhas de uma tabela, começando na posição atual do cursor.  <br/> |
|Anular** <br/> |Para todas as operações assíncronas atualmente em andamento para a tabela.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Expande uma categoria de tabela recolhida, adicionando as linhas de folha pertencentes à categoria para o modo de exibição de tabela.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Recolhe uma categoria de tabela expandida, removendo as linhas de folha pertencentes à categoria do modo de exibição de tabela.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspende o processamento até que uma ou mais operações assíncronas em andamento na tabela tenham sido concluídas.  <br/> |
|[GetCollapsestate](imapitable-getcollapsestate.md) <br/> |Retorna os dados necessários para reconstruir o estado atual recolhido ou expandido de uma tabela categorizada.  <br/> |
|[SetCollapsestate](imapitable-setcollapsestate.md) <br/> |Recria o estado atual expandido ou recolhido de uma tabela categorizada usando dados que foram salvos por uma chamada anterior para o método **IMAPITable::** getcollapsestate.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

