---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435345"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém a pasta que foi estabelecida como o destino para mensagens de entrada de uma classe de mensagem especificada ou como a pasta de recebimento padrão para o armazenamento de mensagens.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Parâmetros

 _lpszMessageClass_
  
> [in] Um ponteiro para uma classe de mensagem que está associada a uma pasta de recebimento. Se o  _parâmetro lpszMessageClass_ for definido como NULL ou uma cadeia de caracteres vazia, **GetReceiveFolder** retornará a pasta de recebimento padrão para o armazenamento de mensagens. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas e retornadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> A cadeia de caracteres de classe de mensagem está no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, a cadeia de caracteres da classe de mensagem está no formato ANSI.
    
 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo _parâmetro lppEntryID._ 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada para a pasta de recebimento solicitada.
    
 _lppszExplicitClass_
  
> [out] Um ponteiro para um ponteiro para a classe de mensagem que define explicitamente como sua pasta de recebimento a pasta apontada por  _lppEntryID_. Essa classe de mensagem deve ser a mesma que a classe no parâmetro  _lpszMessageClass_ ou uma classe base dessa classe. Passar NULL indica que a pasta apontada por  _lppEntryID_ é a pasta de recebimento padrão para o armazenamento de mensagens. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta de recebimento foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::GetReceiveFolder** obtém o identificador de entrada de uma pasta de recebimento, uma pasta designada para receber mensagens de entrada de uma classe de mensagem específica. Os chamadores podem especificar uma classe de mensagem ou NULL no _parâmetro lpszMessageClass._ Se  _lpszMessageClass_ for NULL, **GetReceiveFolder** retornará os seguintes valores: 
  
- Em  _lppszExplicitClass_, o nome da primeira classe base da classe de mensagem apontado por  _lpszMessageClass_ que faz explicitamente definir uma pasta de recebimento. 
    
- Em _lppEntryID_, o identificador de entrada da pasta de recebimento para a classe base apontado pelo _parâmetro lppszExplicitClass._ 
    
Por exemplo, suponha que a pasta de recebimento do IPM da classe de **mensagens. Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM. Note.Phone**. Se **IPM. Note.Phone** não tem uma pasta de recebimento explícita definida, **GetReceiveFolder** retorna o identificador de entrada da Caixa de Entrada em  _lppEntryID_ e **IPM. Observação** em  _lppszExplicitClass_.
  
Se o cliente chamar **GetReceiveFolder** para uma classe de mensagem e não tiver definido uma pasta de recebimento para essa classe de mensagem, _lppszExplicitClass_ será uma cadeia de caracteres de comprimento zero, uma cadeia de caracteres no formato Unicode ou uma cadeia de caracteres no formato ANSI, dependendo se o cliente definiu o sinalizador MAPI_UNICODE no _parâmetro ulFlags._ 
  
Uma pasta de recebimento padrão, obtida passando NULL no parâmetro  _lpszMessageClass,_ sempre existe para cada armazenamento de mensagens. 
  
Um cliente deve chamar a função [MAPIFreeBuffer](mapifreebuffer.md) quando for feito com o identificador de entrada retornado em  _lppEntryID_ para liberar a memória que mantém esse identificador de entrada. Ele também deve chamar **MAPIFreeBuffer** quando for feito com a cadeia de caracteres de classe de mensagem retornada em  _lppszExplicitClass_ para liberar a memória que contém essa cadeia de caracteres. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI usa o **método IMsgStore::GetReceiveFolder** para localizar a pasta Caixa de Entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

