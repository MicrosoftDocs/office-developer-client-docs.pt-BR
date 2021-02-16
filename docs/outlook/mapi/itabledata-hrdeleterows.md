---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416451"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui várias linhas de tabela.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a exclusão. O sinalizador a seguir pode ser definido:
    
TAD_ALL_ROWS 
  
> Exclui todas as linhas da tabela e todos os exibições correspondentes, enviando uma única TABLE_RELOAD de exibição.
    
 _lprowsetToDelete_
  
> [in] Um ponteiro para um conjunto de linhas que descreve as linhas a serem excluídas. O _parâmetro lprowsetToDelete_ poderá ser NULL se o sinalizador TAD_ALL_ROWS for definido no _parâmetro ulFlags._ 
    
 _cRowsDeleted_
  
> [out] A contagem das linhas excluídas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As linhas da tabela foram excluídas com êxito.
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrDeleteRows** localiza e remove as linhas da tabela que contêm as colunas que corresponderem à propriedade apontada pelo membro **lpProps** de cada entrada **aRow** no conjunto de linhas. Uma coluna de índice é usada para identificar cada linha; essa coluna deve ter a mesma marca de propriedade que a marca de propriedade passada no _parâmetro ulPropTagIndexColumn_ na chamada para a [função CreateTable.](createtable.md) 
  
O número de linhas que foram realmente excluídas é retornado em  _cRowsDeleted_. Nenhum erro será retornado se uma ou mais linhas não puderem ser encontradas. 
  
Depois que as linhas são excluídas, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que tenham chamado o método [IMAPITable::Advise](imapitable-advise.md) da tabela para registrar para notificações. 
  
A exclusão de linhas não reduz as colunas disponíveis para exibições de tabela existentes ou exibições de tabela abertas subsequentemente, mesmo que as linhas excluídas sejam as últimas com valores para uma coluna específica.
  
## <a name="see-also"></a>Confira também



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

