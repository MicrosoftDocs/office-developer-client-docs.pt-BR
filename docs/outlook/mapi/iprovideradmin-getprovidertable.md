---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434470"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de provedores do serviço de mensagens, uma lista dos provedores de serviços no serviço de mensagens.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres retornadas nas colunas da tabela do provedor. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, as colunas estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela do provedor.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela do provedor foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin::GetProviderTable** recupera um ponteiro para a tabela do provedor do serviço de mensagens, uma tabela que o MAPI mantém que contém informações sobre cada provedor de serviços no serviço de mensagens. 
  
Ao contrário da tabela de provedor retornada pelo método [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) a tabela de provedor retornada por **IProviderAdmin::GetProviderTable** pode incluir linhas adicionais que representam informações associadas a um ou mais provedores de serviços no serviço de mensagens. Essas informações extras são adicionadas ao perfil com a palavra-chave "Sections" do arquivo Mapisvc.inf. Quando um provedor tem seções de perfil extras, ele armazena as estruturas **MAPIUID** para essas seções na propriedade **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** é salvo na seção de perfil de serviço de mensagens. 
  
Os provedores que foram excluídos ou estão em uso, mas foram marcados para exclusão, não estão incluídos na tabela do provedor. As tabelas de provedor são estáticas, o que significa que as adições ou exclusões subsequentes do serviço de mensagens não são refletidas na tabela. 
  
Se o serviço de mensagens não tiver provedores, **IProviderAdmin::GetProviderTable** retornará uma tabela com zero linhas e o S_OK de retorno. 
  
A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
Para uma lista completa das colunas na tabela do provedor, consulte [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar as linhas de uma tabela de provedor em ordem de transporte, classificar a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Para recuperar apenas as linhas que representam provedores de serviços (sem incluir nenhuma linha extra), limite sua recuperação às linhas que tenham um valor de PT_ERROR na coluna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI usa o método **IProviderAdmin::GetProviderTable** para obter a tabela de provedores para renderizar em uma nova caixa de diálogo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

