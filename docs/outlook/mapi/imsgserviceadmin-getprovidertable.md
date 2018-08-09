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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4272edef5b1b72944d1d27f0e4dd99ee4956aa57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767467"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Aplica-se a**: Outlook 
  
Fornece acesso à tabela de provedor, uma lista de provedores de serviços de perfil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Sempre nulo.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de provedor.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de provedor foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::GetProviderTable** fornece acesso à tabela de provedor MAPI, uma tabela que lista todos os catálogos de endereços, armazenamento de mensagens e provedores de transporte instalados atualmente no perfil. 
  
Ao contrário da tabela de provedor retornada por meio do método [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) , a tabela de provedor retornada por meio de **IMsgServiceAdmin::GetProviderTable** não é possível incluir linhas adicionais que representam informações associadas com um ou mais provedores de serviços no perfil. 
  
Os provedores que forem excluídos, ou estiverem em uso, foram marcados para exclusão, mas não são incluídos na tabela de provedor. As tabelas de provedor são estáticas, o que significa que subsequentes adições à ou exclusões do perfil não são refletidas na tabela. 
  
Se o perfil não tiver nenhum provedor, **GetProviderTable** retornará uma tabela com zero linhas e o valor de retorno S_OK. 
  
Para obter uma lista completa das colunas da tabela de provedor, consulte a [Tabela de provedor](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar as linhas de uma tabela de provedor na ordem de transporte, use o procedimento a seguir:
  
1. Chame o método [IMAPITable:: Restrict](imapitable-restrict.md) para impor uma restrição de propriedade que corresponda a propriedade **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) com MAPI_TRANSPORT_PROVIDER.
    
2. Chame o método [IMAPITable:: SortTable](imapitable-sorttable.md) para classificar a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Chame o método [IMAPITable:: QueryRows](imapitable-queryrows.md) para obter as linhas da tabela. 
    
Uma alternativa para essas chamadas é tornar uma única chamada para a função [HrQueryAllRows](hrqueryallrows.md) com todos os dados apropriados estruturas passadas. 
  
Se você recuperar as colunas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) em cada uma das linhas, você pode usar essa matriz de estruturas **MAPIUID** para definir a ordem de transporte em uma chamada para [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ faz o seguinte: 
  
- Define o tipo de cadeia de caracteres para Unicode para os dados retornados para colunas ativas iniciais da tabela provedor pelo método [IMAPITable::QueryColumns](imapitable-querycolumns.md) . Colunas ativas iniciais para uma tabela de provedor são as colunas que o método **QueryColumns** retorna antes do provedor que contém as chamadas de tabela o método [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- Define o tipo de cadeia de caracteres para Unicode para os dados retornados para as linhas de ativas iniciais da tabela provedor por **QueryRows**. As linhas de ativas iniciais para uma tabela de provedor são aquelas linhas **que QueryRows** retorna antes do provedor que contém as chamadas de tabela **SetColumns**. 
    
- Controles os tipos de propriedade da ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) antes que o cliente que contém a tabela de provedor chama o método [IMAPITable:: SortTable](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

