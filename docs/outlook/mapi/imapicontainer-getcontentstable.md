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
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431103"
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
  
> no Uma bitmask de sinalizadores que controla como a tabela de conteúdo é retornada. Os seguintes sinalizadores podem ser definidos:
    
MAPI_ASSOCIATED 
  
> A tabela de conteúdo associado do contêiner deve ser retornada em vez da tabela de conteúdo padrão. Este sinalizador é usado somente com pastas. As mensagens incluídas na tabela de conteúdo associado foram criadas com o sinalizador MAPI_ASSOCIATED definido na chamada para o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . Normalmente, os clientes usam a tabela de conteúdo associado para recuperar formulários, exibições e outras mensagens ocultas. 
    
ACLTABLE_FREEBUSY
  
> Permite o acesso aos direitos frightsFreeBusySimple e frightsFreeBusyDetailed no **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **** Getcontenttable pode ser retornado com êxito, possivelmente antes de a tabela ser disponibilizada para o chamador. Se a tabela não estiver disponível, fazer uma chamada de tabela subsequente poderá gerar um erro. 
    
MAPI_UNICODE 
  
> Solicita que as colunas que contêm dados de cadeia de caracteres sejam retornadas no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres deverão ser retornadas no formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Mostra os itens atualmente marcados como excluídos por software, ou seja, estão na fase de tempo de retenção de item excluído.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela de conteúdo.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de conteúdo foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O contêiner não tem conteúdo e não pode fornecer uma tabela de conteúdo.
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer::** getcontenttable retorna um ponteiro para a tabela de conteúdo de um contêiner. Uma tabela de conteúdo contém informações de resumo sobre objetos no contêiner. 
  
As tabelas de conteúdo têm conjuntos de colunas longos. Para obter uma lista completa das colunas obrigatórias e opcionais nas tabelas de conteúdo, consulte [tabelas de conteúdo](contents-tables.md). 
  
É possível que alguns contêineres não tenham conteúdo. Esses contêineres retornam MAPI_E_NO_SUPPORT de suas **** implementações de getcontenttable.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você oferecer suporte a uma tabela de conteúdo para seu contêiner, também deverá fazer o seguinte:
  
- Suporte a chamadas para o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Retornar **PR_CONTAINER_CONTENTS** em resposta a uma chamada para o contêiner do 
    
    [IMAPIProp::](imapiprop-getprops.md) GetProps e [IMAPIProp::](imapiprop-getproplist.md) getproplist métodos. 
    
A implementação de um provedor de transporte remoto desse método deve retornar um ponteiro para uma interface imApitable [: IUnknown](imapitableiunknown.md) no parâmetro _ppTable_ passado para o método getcontenttable. **** Se o seu provedor de transporte tiver uma tabela de conteúdo existente, será suficiente retornar um ponteiro para ela. Caso contrário, esse método deve criar um novo objeto imApitable [: IUnknown](imapitableiunknown.md) , preencher a tabela com cabeçalhos de mensagem (se houver algum disponível) e retornar um ponteiro para a nova tabela. O método [ITableData:: HrGetView](itabledata-hrgetview.md) é útil para gerar um valor de retorno e armazenar o ponteiro de tabela no parâmetro _ppTable_ . A tabela de conteúdo deve suportar pelo menos as seguintes colunas de propriedade: 
  
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

As colunas da tabela de conteúdo binário e cadeia de caracteres podem ser truncadas. Normalmente, os provedores retornam 255 caracteres. Como você não pode saber antecipadamente se uma tabela inclui colunas truncadas, suponha que uma coluna será truncada se o comprimento da coluna for 255 ou 510 bytes. Você sempre pode recuperar o valor completo de uma coluna truncada, se necessário, diretamente do objeto usando seu identificador de entrada para abri-lo e, em seguida, chamando o método **IMAPIProp::** GetProps. 
  
Dependendo da implementação do provedor, as operações de classificação e restrições podem ser aplicadas a todas as cadeias de caracteres ou à versão truncada dessa cadeia de caracteres.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableDialog. cpp  <br/> |CContentsTableDlg:: CContentsTableDlg  <br/> |A classe **CContentsTableDlg** usa **** getcontenttable para obter as entradas em uma tabela de conteúdo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

