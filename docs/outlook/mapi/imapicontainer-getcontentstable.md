---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9fb8919287420038b5c9165bb14b7d33d1ad2fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578861"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para a tabela de conteúdo do contêiner.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a tabela de conteúdo é retornada. Sinalizadores a seguir podem ser definidos:
    
MAPI_ASSOCIATED 
  
> Tabela de conteúdo associado do contêiner deve ser retornada no lugar do índice de conteúdo padrão. Esse sinalizador é usado somente com as pastas. As mensagens que estão incluídas na tabela de conteúdo associado foram criadas com o sinalizador MAPI_ASSOCIATED definido na chamada para o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Clientes normalmente usam a tabela de conteúdo associado para recuperar a formulários, exibições e outras mensagens ocultas. 
    
ACLTABLE_FREEBUSY
  
> Permite o acesso aos direitos de frightsFreeBusySimple e frightsFreeBusyDetailed em **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** pode retornar com êxito, possivelmente antes que a tabela é disponibilizada para o chamador. Se a tabela não estiver disponível, fazendo uma chamada de tabela subsequentes pode gerar um erro. 
    
MAPI_UNICODE 
  
> Solicitações que as colunas que contêm dados de cadeia de caracteres a ser retornado no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem ser retornadas no formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Mostra os itens que estão marcados como suaves excluídos — ou seja, eles estão na retenção de item excluído fase de tempo.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de conteúdo.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de conteúdo foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O contêiner não tiver conteúdo e não pode fornecer uma tabela de conteúdo.
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer::GetContentsTable** retorna um ponteiro para o índice de conteúdo de um contêiner. Uma tabela de conteúdo contém informações de resumo sobre objetos no contêiner. 
  
Tabelas de conteúdo têm conjuntos de coluna longos. Para obter uma lista completa das colunas obrigatórios e opcionais nas tabelas de conteúdo, consulte [As tabelas de conteúdo](contents-tables.md). 
  
É possível que alguns contêineres ter nenhum conteúdo. Desses contêineres retornam MAPI_E_NO_SUPPORT de suas implementações de **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Caso você ofereça suporte a uma tabela de conteúdo para seu contêiner, você deve também faça o seguinte:
  
- Suporte a chamadas para o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Retornar **PR_CONTAINER_CONTENTS** em resposta a uma chamada para o contêiner 
    
    Métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
Implementação de um provedor de transporte remoto deste método deve retornar um ponteiro para uma [IMAPITable: IUnknown](imapitableiunknown.md) interface no parâmetro _ppTable_ passado para o método **GetContentsTable** . Se o seu provedor de transporte tem uma tabela de conteúdo existente, é suficiente para retornar um ponteiro para ele. Se não, esse método deve criar um novo [IMAPITable: IUnknown](imapitableiunknown.md) do objeto, preenchem a tabela com cabeçalhos de mensagem (caso haja algum disponível) e retornar um ponteiro para a nova tabela. O método [ITableData::HrGetView](itabledata-hrgetview.md) é útil para gerar um valor de retorno e armazenar o ponteiro de tabela no parâmetro _ppTable_ . A tabela de conteúdo deve suportar pelo menos as seguintes colunas de propriedade: 
  
- **PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>Notas para chamadores

Cadeia de caracteres e binário colunas da tabela de conteúdo podem ser truncadas. Normalmente, provedores retornam 255 caracteres. Porque você não pode saber com antecedência se uma tabela inclui colunas truncadas, suponha que uma coluna será truncada se o comprimento da coluna é 255 ou 510 bytes. Você sempre pode recuperar o valor completo de uma coluna truncado, se necessário, diretamente do objeto utilizando seu identificador de entrada para abri-lo e, em seguida, chamando o método **IMAPIProp::GetProps** . 
  
Dependendo da implementação do provedor, restrições e operações de classificação podem aplicar a todas de uma cadeia de caracteres ou para a versão truncada da cadeia de caracteres.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |A classe **CContentsTableDlg** usa **GetContentsTable** para obter as entradas em uma tabela de conteúdo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

