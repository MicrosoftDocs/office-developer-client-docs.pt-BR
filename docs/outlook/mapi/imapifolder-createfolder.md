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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436759"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parâmetros

 _ulFolderType_
  
> [in] O tipo de pasta a ser criado. Os sinalizadores a seguir podem ser definidos:
    
FOLDER_GENERIC 
  
> Uma pasta genérica deve ser criada.
    
FOLDER_SEARCH 
  
> Uma pasta de resultados de pesquisa deve ser criada.
    
 _lpszFolderName_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o nome da nova pasta. Esse nome é a base para a propriedade PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) da nova pasta.
    
 _lpszFolderComment_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém um comentário associado à nova pasta. Essa cadeia de caracteres se torna o valor da propriedade PR_COMMENT **(** [PidTagComment](pidtagcomment-canonical-property.md)) da nova pasta. Se NULL for passado, a pasta não terá comentários iniciais.
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a nova pasta. Passar NULL faz com que o provedor de armazenamento de mensagens retorne a interface de pasta padrão, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Os clientes devem passar NULL. Outros chamadores podem definir o  _parâmetro lpInterface_ como IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a pasta é criada. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **CreateFolder** retorne com êxito, possivelmente antes da nova pasta estar totalmente disponível para o cliente de chamada. Se a nova pasta não estiver disponível, fazer uma chamada subsequente pode causar um erro. 
    
MAPI_UNICODE 
  
> O nome da pasta está no formato Unicode. Se o MAPI_UNICODE não estiver definido, o nome da pasta está no formato ANSI.
    
OPEN_IF_EXISTS 
  
> Permite que o método tenha êxito mesmo se a pasta nomeada no parâmetro  _lpszFolderName_ já existir abrindo a pasta existente com esse nome. Observe que os provedores de armazenamento de mensagens que permitem que pastas irmãos tenham o mesmo nome podem não abrir uma pasta existente se houver mais de um com o nome fornecido. 
    
 _lppFolder_
  
> [out] Um ponteiro para um ponteiro para a pasta recém-criada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova pasta foi criada ou aberta com êxito, se o sinalizador OPEN_IF_EXISTS estiver definido.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
MAPI_E_COLLISION 
  
> Já existe uma pasta com o nome dado _no parâmetro lpszFolderName._ Os nomes das pastas devem ser exclusivos. 
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::CreateFolder** cria uma subpasta na pasta atual e atribui um identificador de entrada à nova pasta. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **CreateFolder** retornar, esteja ciente de que o identificador de entrada para a nova pasta pode não estar disponível. Alguns provedores de armazenamento de mensagens não disponibilizam identificadores de entrada até que você tenha chamado o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova pasta para salvá-la permanentemente. Isso é especialmente verdadeiro se você tiver definido o MAPI_DEFERRED_ERRORS sinalizador. 
  
Saiba que alguns provedores de armazenamento de mensagens sempre apontam o parâmetro _lppFolder_ para a interface padrão da pasta, independentemente do valor que você passa para o parâmetro _lpInterface._ Como o ponteiro da interface retornado pode não ser do tipo esperado, chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) da nova pasta para recuperar a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Se necessário, cast the pointer to a more appropriate type before you make other calls.
  
A maioria dos provedores de armazenamento de mensagens exige que o nome da nova pasta seja exclusivo em relação aos nomes de suas pastas irmãos. Ser capaz de manipular o MAPI_E_COLLISION de erro, que será retornado se essa regra não for seguida. 
  
Para determinar o identificador de entrada da pasta recém-criada, chame o método **IMAPIProp::GetProps** da nova pasta para recuperar sua **propriedade PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI usa o **método CMsgStoreDlg::OnCreateSubFolder** para criar novas pastas em MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

