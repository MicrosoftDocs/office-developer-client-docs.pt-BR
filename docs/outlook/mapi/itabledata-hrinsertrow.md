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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435436"
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
  
> [in] Um número de linha sequencial que representa uma linha específica. A nova linha será colocada após a linha indicada pelo número. O  _parâmetro uliRow_ pode conter números de linha de 0 a n, onde n é o número total de linhas na tabela. Passar n  _em uliRow_ anexa a linha ao final da tabela. 
    
 _lpSRow_
  
> [in] Um ponteiro para uma [estrutura SRow](srow.md) que descreve a linha a ser inserida. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A linha foi inserida com êxito.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma linha que tem o mesmo valor de sua coluna de índice que a linha a ser inserida já existe na tabela.
    
## <a name="remarks"></a>Comentários

O **método ITableData::HrInsertRow** insere uma linha em uma tabela em uma posição específica. A nova linha é inserida após a linha que está na posição especificada pelo _parâmetro uliRow._ 
  
Se  _uliRow_ for definido como o número de linhas na tabela, a nova linha será anexada ao final da tabela. 
  
A propriedade que atua como coluna de índice para a tabela deve ser incluída no membro **lpProps** da estrutura [SRow](srow.md) apontada pelo _parâmetro lpSRow._ Essa propriedade de índice, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), é usada para identificar exclusivamente a linha para tarefas de manutenção futuras.
  
As colunas de propriedades na **estrutura SRow** não devem estar na mesma ordem que as colunas de propriedades na tabela. 
  
Depois que a linha é inserida, as notificações são enviadas a todos os clientes ou provedores de serviços que têm um modo de exibição da tabela e que tenham chamado o método [IMAPITable::Advise](imapitable-advise.md) da tabela para registrar para notificações. Nenhuma notificação será enviada se a linha inserida não for incluída no visualização devido a uma restrição. 
  
## <a name="see-also"></a>Confira também



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

