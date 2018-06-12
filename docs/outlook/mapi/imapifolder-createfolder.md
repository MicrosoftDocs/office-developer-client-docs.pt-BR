---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 36fd729b1ca3e5d877d03358d581b83fc6d4782c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766976"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Aplica-se a**: Outlook 
  
Cria uma nova subpasta.
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a>Par�metros

 _ulFolderType_
  
> [in] O tipo da pasta a ser criada. Sinalizadores a seguir podem ser definidos:
    
FOLDER_GENERIC 
  
> Uma pasta genérica deve ser criada.
    
FOLDER_SEARCH 
  
> Uma pasta de resultados de pesquisa deve ser criada.
    
 _lpszFolderName_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o nome da nova pasta. Esse nome é a base para a propriedade de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) da nova pasta.
    
 _lpszFolderComment_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém um comentário associado a nova pasta. Esta cadeia de caracteres torna-se o valor da propriedade de **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) da nova pasta. Se NULL for passado, a pasta não tem nenhum comentário inicial.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a nova pasta. Passar NULL faz com que o provedor de armazenamento de mensagem retornar a interface de pasta padrão, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Os clientes devem passar NULL. Outros chamadores podem definir o parâmetro _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a pasta é criada. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **CreateFolder** retornar com êxito, possivelmente antes que a nova pasta esteja totalmente disponível para o cliente da chamada. Se a nova pasta não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro. 
    
MAPI_UNICODE 
  
> O nome da pasta é no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta é no formato ANSI.
    
OPEN_IF_EXISTS 
  
> Permite que o método seja bem-sucedido, mesmo se a pasta chamada no parâmetro _lpszFolderName_ já existe abrindo a pasta existente que recebeu esse nome. Observe que os provedores de armazenamento de mensagem que permitem irmão pastas para ter o mesmo nome não podem abrir uma pasta existente se mais de um existir com o nome fornecido. 
    
 _lppFolder_
  
> [out] Um ponteiro para um ponteiro para a pasta recém-criada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A nova pasta foi criada ou aberta, se o sinalizador OPEN_IF_EXISTS for definido com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_COLLISION 
  
> Uma pasta que tem o nome fornecido no parâmetro _lpszFolderName_ já existe. Nomes de pasta devem ser exclusivos. 
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIFolder::CreateFolder** cria uma subpasta na pasta atual e atribui um identificador de entrada para a nova pasta. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **CreateFolder** retorna, lembre-se de que o identificador de entrada para a nova pasta pode não estar disponível. Alguns provedores de armazenamento de mensagem não disponibilizar identificadores de entrada até depois de ter chamado o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova pasta para permanentemente salvá-la. Isso acontece principalmente se você tiver configurado o sinalizador MAPI_DEFERRED_ERRORS. 
  
Lembre-se de que alguns provedores de armazenamento de mensagem sempre apontam o parâmetro _lppFolder_ para interface de padrão da pasta, independentemente do valor que você passa para o parâmetro _lpInterface_ . Porque o ponteiro de interface retornada pode não ser do tipo que você espera, chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da nova pasta para recuperar a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Se necessário, converta o ponteiro para um tipo mais apropriado antes de fazer outras chamadas.
  
A maioria dos provedores de armazenamento de mensagem exigem o nome da nova pasta seja exclusivo com relação aos nomes das suas pastas irmão. Ser capaz de manipular o valor de erro do MAPI_E_COLLISION, será retornado se esta regra não é seguida. 
  
Para determinar o identificador de entrada da pasta recém-criada, chame o método de **IMAPIProp::GetProps** da nova pasta para recuperar sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI usa o método **CMsgStoreDlg::OnCreateSubFolder** para criar novas pastas no MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

