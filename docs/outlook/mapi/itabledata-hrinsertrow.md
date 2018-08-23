---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9aa038958e26652ae7ead728ab15d068e080dc69
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579883"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Insere uma linha de tabela. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parâmetros

 _uliRow_
  
> [in] Um número de linha sequencial que representa uma linha específica. Após a linha que indica o número será colocada a nova linha. O parâmetro _uliRow_ pode conter os números de linha de 0 até n, onde n é o número total de linhas da tabela. Passando n _uliRow_ acrescenta a linha no final da tabela. 
    
 _lpSRow_
  
> [in] Um ponteiro para uma estrutura de [SRow](srow.md) que descreve a linha a ser inserido. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A linha foi inserida com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma linha que tem o mesmo valor para a coluna de seu índice, como a linha a ser inserido já existe na tabela.
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrInsertRow** insere uma linha em uma tabela em uma posição específica. A nova linha é inserida após a linha que está na posição especificada pelo parâmetro _uliRow_ . 
  
Se _uliRow_ for definido como o número de linhas na tabela, a nova linha é acrescentada ao final da tabela. 
  
A propriedade que atua como a coluna de índice para a tabela deve ser incluída no membro **lpProps** da estrutura [SRow](srow.md) apontado pelo parâmetro _lpSRow_ . Esta propriedade index, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é usada para identificar exclusivamente a linha para tarefas de manutenção futura.
  
As colunas de propriedades na estrutura de **SRow** não precisará ser na mesma ordem como as colunas de propriedades da tabela. 
  
Depois que a linha é inserida, as notificações são enviadas para todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que chamou o método da tabela [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações. Nenhuma notificação é enviada se a linha inserida não está incluída no modo de exibição devido a uma restrição. 
  
## <a name="see-also"></a>Confira também



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

