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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398707"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um modo de exibição de tabela, retornando um ponteiro para uma implementação [IMAPITable](imapitableiunknown.md) . 
  
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
  
> [in] Um ponteiro para uma estrutura de ordem de classificação que descreve a ordem de classificação para o modo de exibição de tabela. Se o parâmetro _lpSSortOrderSet_ é passado NULL, o modo de exibição não será classificado. 
    
 _lpfCallerRelease_
  
> [in] Um ponteiro para uma função de retorno de chamada com base em protótipo [CALLERRELEASE](callerrelease.md) que chamadas MAPI quando ele libera o modo de exibição. Se NULL é passada no parâmetro _lpfCallerRelease_ , nenhuma função é chamada na versão do modo de exibição. 
    
 _ulCallerData_
  
> [in] Os dados que devem ser passados para a função de retorno de chamada apontada pela _lpfCallerRelease_e salvo com o novo modo de exibição.
    
 _lppMAPITable_
  
> [out] Um ponteiro para um ponteiro para o modo de exibição recém-criado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O modo de exibição foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **ITableData::HrGetView** cria uma exibição somente leitura dos dados na tabela, classificada na ordem apontada pelo parâmetro _lpSSortOrderSet_ . O cursor é colocado no início da primeira linha no modo de exibição. Uma implementação de interface **IMAPITable** para acessar o modo de exibição será retornada. 
  
Provedores de serviços de chamarem **HrGetView** sempre que precisarem dar um acesso para cliente a uma tabela. **HrGetView** cria o modo de exibição e retorna o ponteiro **IMAPITable** . Provedores de serviços por sua vez passam o ponteiro para o cliente. Quando o cliente for concluído, usando a tabela e chama o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** chama a função de retorno de chamada apontada pelo parâmetro _lpfCallerRelease_ . 
  
Se precisa de um provedor de serviços retornar a um cliente de um modo de exibição que tenha uma coluna personalizada definida ou uma restrição, o provedor pode chamar métodos do modo de exibição de [IMAPITable::SetColumns](imapitable-setcolumns.md) e [IMAPITable:: Restrict](imapitable-restrict.md) antes de permitir o acesso do cliente. 
  
## <a name="see-also"></a>Confira também



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

