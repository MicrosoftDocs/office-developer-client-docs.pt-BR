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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278944"
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
  
> no Uma bitmask de sinalizadores que controlam a exclusão. O seguinte sinalizador pode ser definido:
    
TAD_ALL_ROWS 
  
> Exclui todas as linhas da tabela e de todos os modos de exibição correspondentes, enviando uma única notificação de TABLE_RELOAD.
    
 _lprowsetToDelete_
  
> no Um ponteiro para um conjunto de linhas que descreve as linhas a serem excluídas. O parâmetro _lprowsetToDelete_ pode ser NULL se o sinalizador TAD_ALL_ROWS estiver definido no parâmetro _parâmetroulflags_ . 
    
 _cRowsDeleted_
  
> bota A contagem das linhas excluídas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As linhas da tabela foram excluídas com êxito.
    
## <a name="remarks"></a>Comentários

O método **ITableData:: HrDeleteRows** localiza e remove as linhas da tabela que contêm as colunas que correspondem à propriedade indicada pelo membro **lpProps** de cada entrada **aRow** no conjunto de linhas. Uma coluna de índice é usada para identificar cada linha; Essa coluna deve ter a mesma marca de propriedade que a marca de propriedade passada no parâmetro _ulPropTagIndexColumn_ na chamada para a [](createtable.md) função CreateTable. 
  
O número de linhas realmente excluídas é retornado em _cRowsDeleted_. Nenhum erro será retornado se não foi possível localizar uma ou mais linhas. 
  
Depois que as linhas são excluídas, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamaram o método imApitable [:: Advise](imapitable-advise.md) a ser registrado para notificações. 
  
A exclusão de linhas não reduz as colunas disponíveis para os modos de exibição de tabelas existentes ou, subsequentemente, abrir modos de exibição de tabela, mesmo que as linhas excluídas sejam a última que tenham valores para uma coluna específica.
  
## <a name="see-also"></a>Confira também



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

