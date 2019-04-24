---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278712"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um modo de exibição de tabela, retornando [](imapitableiunknown.md) um ponteiro para uma implementação IMAPITable. 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Parâmetros

 _lpSSortOrderSet_
  
> no Um ponteiro para uma estrutura de ordem de classificação que descreve a ordem de classificação para o modo de exibição de tabela. Se NULL é passado no parâmetro _lpSSortOrderSet_ , o modo de exibição não é classificado. 
    
 _lpfCallerRelease_
  
> no Um ponteiro para uma função de retorno de chamada com base no protótipo [CALLERRELEASE](callerrelease.md) que MAPI chama quando libera o modo de exibição. Se NULL for passado no parâmetro _lpfCallerRelease_ , nenhuma função será chamada no lançamento do modo de exibição. 
    
 _ulCallerData_
  
> no Os dados que devem ser salvos com o novo modo de exibição e passados para a função de retorno de chamada indicada por _lpfCallerRelease_.
    
 _lppMAPITable_
  
> bota Um ponteiro para um ponteiro para o modo de exibição recém-criado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O modo de exibição foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **ITableData:: HrGetView** cria um modo de exibição somente leitura dos dados na tabela, classificados na ordem indicada pelo parâmetro _lpSSortOrderSet_ . O cursor é colocado no início da primeira linha no modo de exibição. Uma **** implementação de interface imapitada para acessar o modo de exibição é retornada. 
  
Os provedores de serviços chamam o **HrGetView** quando precisam dar acesso ao cliente a uma tabela. **HrGetView** cria o modo de exibição e **** retorna o ponteiro IMAPITable. Os provedores de serviços, por sua vez, passam o ponteiro para o cliente. Quando o cliente termina de usar a tabela e chama seu método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** chama a função de retorno de chamada apontada pelo parâmetro _lpfCallerRelease_ . 
  
Se um provedor de serviços precisar retornar a um cliente um modo de exibição que tenha um conjunto de colunas ou uma restrição personalizada, o provedor poderá chamar o [método IMAPITable::](imapitable-setcolumns.md) SetColumns e IMAPITable [:: Restrict](imapitable-restrict.md) Methods antes de permitir o acesso do cliente. 
  
## <a name="see-also"></a>Confira também



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

