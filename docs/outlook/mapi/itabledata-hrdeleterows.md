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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767704"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Aplica-se a**: Outlook 
  
Exclui a várias linhas de tabela.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a exclusão. O seguinte sinalizador pode ser definido:
    
TAD_ALL_ROWS 
  
> Exclui todas as linhas da tabela e todos os modos de exibição correspondentes, enviar a notificação de TABLE_RELOAD única.
    
 _lprowsetToDelete_
  
> [in] Um ponteiro para um conjunto de linha que descreve as linhas a ser excluído. O parâmetro _lprowsetToDelete_ pode ser NULL se o sinalizador TAD_ALL_ROWS é definido no parâmetro _ulFlags_ . 
    
 _cRowsDeleted_
  
> [out] A contagem de linhas excluídas.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As linhas de tabela foram excluídas com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **ITableData::HrDeleteRows** localiza e remove as linhas de tabela que contêm as colunas que coincidem com a propriedade apontada para pelo membro de cada entrada de **aRow** na linha **lpProps** definir. Uma coluna de índice é usada para identificar cada linha; Essa coluna deve ter a mesma marca de propriedade, como a marca de propriedade passada no parâmetro _ulPropTagIndexColumn_ na chamada para a função [CreateTable](createtable.md) . 
  
O número de linhas que foram excluídas realmente é retornado no _cRowsDeleted_. Nenhum erro será retornado se uma ou mais linhas não pôde ser encontradas. 
  
Depois que as linhas são excluídas, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações. 
  
A exclusão de linhas não reduz as colunas disponíveis para modos de exibição de tabela existente ou aberto subsequentemente modos de exibição de tabela, mesmo se as linhas excluídas são a última que têm valores para uma coluna específica.
  
## <a name="see-also"></a>Confira também



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

