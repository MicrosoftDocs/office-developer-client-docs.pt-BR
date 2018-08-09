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
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767659"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Aplica-se a**: Outlook 
  
Fornece acesso à tabela do provedor do serviço na mensagem, uma lista dos provedores de serviço no serviço de mensagem.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornada nas colunas da tabela provedor. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas são no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de provedor.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de provedor foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin::GetProviderTable** recupera um ponteiro para a tabela de provedor do serviço na mensagem, uma tabela que mantém o MAPI que contém informações sobre cada provedor de serviço no serviço de mensagem. 
  
Ao contrário da tabela de provedor retornada pelo método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , a tabela de provedor retornada pela **IProviderAdmin::GetProviderTable** pode incluir linhas adicionais que representam informações associadas a um ou mais dos os provedores de serviço no serviço de mensagem. Essas informações extras são adicionadas ao perfil com a palavra-chave "Seções" do arquivo Mapisvc. Quando um provedor tem seções perfil extra, ele armazena as estruturas de **MAPIUID** para estas seções na propriedade **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** é salvo na seção de perfil de serviço de mensagem. 
  
Os provedores que forem excluídos, ou estiverem em uso, foram marcados para exclusão, mas não são incluídos na tabela de provedor. As tabelas de provedor são estáticas, que significa subsequentes adições à ou exclusões do serviço de mensagem não serão refletidas na tabela. 
  
Se o serviço de mensagem não tiver nenhum provedor, **IProviderAdmin::GetProviderTable** retornará uma tabela com zero linhas e o valor de retorno S_OK. 
  
Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
Para obter uma lista completa das colunas da tabela de provedor, consulte a [Tabela de provedor](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar as linhas de uma tabela de provedor na ordem de transporte, classifica a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Para recuperar apenas as linhas que representam os provedores de serviços (sem incluindo qualquer linha extra), limite sua recuperação às linhas que possuem um valor de PT_ERROR na sua coluna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI usa o método **IProviderAdmin::GetProviderTable** para obter a tabela de provedores para renderizar em uma nova caixa de diálogo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

