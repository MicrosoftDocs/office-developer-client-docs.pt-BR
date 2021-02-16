---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428764"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela do provedor, uma listagem dos provedores de serviços no perfil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Sempre NULO.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela do provedor.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela do provedor foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::GetProviderTable** fornece acesso à tabela de provedores MAPI, uma tabela que lista todos os provedores de transporte, armazenamento de mensagens e agendamento de endereços atualmente instalados no perfil. 
  
Ao contrário da tabela de provedor retornada por meio do método [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md) a tabela de provedor retornada por meio de **IMsgServiceAdmin::GetProviderTable** não pode incluir linhas adicionais que representam informações associadas a um ou mais provedores de serviços no perfil. 
  
Os provedores que foram excluídos ou estão em uso, mas foram marcados para exclusão, não estão incluídos na tabela do provedor. As tabelas de provedor são estáticas, o que significa que as adições ou exclusões subsequentes do perfil não são refletidas na tabela. 
  
Se o perfil não tiver provedores, **GetProviderTable** retornará uma tabela com zero linhas e o S_OK valor de retorno. 
  
Para uma lista completa das colunas na tabela do provedor, consulte [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar as linhas de uma tabela de provedor em ordem de transporte, use o procedimento a seguir:
  
1. Chame o [método IMAPITable::Restrict](imapitable-restrict.md) para impor uma restrição de propriedade que corresponde à propriedade **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) com MAPI_TRANSPORT_PROVIDER.
    
2. Chame o [método IMAPITable::SortTable](imapitable-sorttable.md) para classificar a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Chame o [método IMAPITable::QueryRows](imapitable-queryrows.md) para obter as linhas da tabela. 
    
Uma alternativa a essas chamadas é fazer uma única chamada para a função [HrQueryAllRows](hrqueryallrows.md) com todas as estruturas de dados apropriadas passadas. 
  
Se você recuperar as colunas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) em cada uma das linhas, poderá usar essa matriz de estruturas **MAPIUID** para definir a ordem de transporte em uma chamada para [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
A definição MAPI_UNICODE sinalizador de configuração no  _parâmetro ulFlags_ faz o seguinte: 
  
- Define o tipo de cadeia de caracteres como Unicode para dados retornados para as colunas ativas iniciais da tabela do provedor pelo método [IMAPITable::QueryColumns.](imapitable-querycolumns.md) As colunas ativas iniciais de uma tabela de provedor são aquelas que o método **QueryColumns** retorna antes do provedor que contém a tabela chamar o método [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- Define o tipo de cadeia de caracteres como Unicode para dados retornados para as linhas ativas iniciais da tabela do provedor **por QueryRows**. As linhas ativas iniciais de uma tabela de provedor são aquelas que **QueryRows** retorna antes do provedor que contém a tabela chama **SetColumns**. 
    
- Controla os tipos de propriedade da ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) antes que o cliente que contém a tabela de provedor chama o método [IMAPITable::SortTable.](imapitable-sorttable.md) 
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

