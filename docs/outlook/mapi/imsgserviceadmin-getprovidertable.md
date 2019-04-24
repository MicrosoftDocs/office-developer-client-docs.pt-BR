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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317378"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela do provedor, uma lista dos provedores de serviços no perfil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Sempre nulo.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela de provedor.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela do provedor foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::** getprovidertable fornece acesso à tabela de provedor MAPI, uma tabela que lista todo o catálogo de endereços, o repositório de mensagens e os provedores de transporte atualmente instalados no perfil. 
  
Diferente da tabela de provedor retornada por meio do método [IProviderAdmin::](iprovideradmin-getprovidertable.md) getprovidertable, a tabela de provedor retornada através de **IMsgServiceAdmin::** getprovidertable não pode incluir linhas adicionais que representam informações associadas com um ou mais provedores de serviço no perfil. 
  
Os provedores que foram excluídos ou estão em uso, mas que foram marcados para exclusão, não estão incluídos na tabela do provedor. As tabelas de provedor são estáticas, o que significa que adições ou exclusões subsequentes do perfil não são refletidas na tabela. 
  
Se o perfil não tiver provedores, **** getprovidertable retornará uma tabela com zero linhas e o valor de retorno de S_OK. 
  
Para obter uma lista completa das colunas na tabela do provedor, consulte [tabela do provedor](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar as linhas de uma tabela de provedor em ordem de transporte, use o seguinte procedimento:
  
1. Chame o método imApitable [:: Restrict](imapitable-restrict.md) para impor uma restrição de propriedade que corresponda à propriedade **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) com MAPI_TRANSPORT_PROVIDER.
    
2. Chame o método imApitable [:: SortTable](imapitable-sorttable.md) para classificar a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Chame o método imApitable [:: QueryRows](imapitable-queryrows.md) para obter as linhas da tabela. 
    
Uma alternativa para essas chamadas é fazer uma única chamada para a função [HrQueryAllRows](hrqueryallrows.md) com todas as estruturas de dados apropriadas passadas. 
  
Se você recuperar as colunas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) em cada uma das linhas, poderá usar essa matriz de estruturas do **MAPIUID** para definir a ordem de transporte em uma chamada para [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ faz o seguinte: 
  
- Define o tipo de cadeia de caracteres como Unicode para dados retornados para as colunas iniciais ativas da tabela do provedor pelo método imApitable [:: QueryColumns](imapitable-querycolumns.md) . As colunas iniciais ativas de uma tabela de provedor são aquelas colunas que o método **QueryColumns** retorna antes de o provedor que contém a tabela chamar o método IMAPITable [::](imapitable-setcolumns.md) SetColumns. 
    
- Define o tipo de cadeia de caracteres como Unicode para dados retornados para as linhas iniciais ativas da tabela do provedor por **QueryRows**. As linhas iniciais ativas de uma tabela de provedor são as linhas que **QueryRows** retorna antes do provedor que contém **** SetColumns de chamadas de tabela. 
    
- Controla os tipos de propriedade da ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) antes de o cliente que contém a tabela do provedor chamar o método IMAPITable [:: SortTable](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

