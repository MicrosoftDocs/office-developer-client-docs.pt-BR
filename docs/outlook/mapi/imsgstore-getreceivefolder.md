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
ms.openlocfilehash: f58bd8499b63bcd526906f78143b76092f194cb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767488"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Aplica-se a**: Outlook 
  
Obtém a pasta que foi estabelecida como pasta para o armazenamento de mensagens de recebimento de destino para mensagens recebidas de uma classe de mensagem especificada ou como padrão.
  
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
  
> [in] Um ponteiro para uma classe de mensagem que está associado uma pasta de recebimento. Se o parâmetro _lpszMessageClass_ for definido como NULL ou como uma sequência vazia, **GetReceiveFolder** retorna o padrão recebem a pasta para o armazenamento de mensagens. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres passada-in e retornados. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> A cadeia de caracteres de classe de mensagem está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres de classe de mensagem é no formato ANSI.
    
 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pasta de recebimento de um ponteiro para um ponteiro para o identificador de entrada para os solicitados.
    
 _lppszExplicitClass_
  
> [out] Um ponteiro para um ponteiro para a classe de mensagem que explicitamente define como seu a pasta indicada por _lppEntryID_de pasta de recebimento. Esta classe de mensagem deve ser o mesmo que a classe no parâmetro _lpszMessageClass_ , ou uma classe base dessa classe. Passar NULL indica que a pasta indicada por _lppEntryID_ é o padrão receber a pasta para o armazenamento de mensagens. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A pasta de recebimento foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::GetReceiveFolder** obtém o identificador de entrada de uma pasta de recebimento, em uma pasta designada para receber mensagens de entrada de uma classe de mensagem específica. Os chamadores podem especificar uma classe de mensagem ou NULL no parâmetro _lpszMessageClass_ . Se _lpszMessageClass_ for NULL, **GetReceiveFolder** retorna os seguintes valores: 
  
- Em _lppszExplicitClass_, o nome da classe primeira base da classe de mensagem apontado pela _lpszMessageClass_ que definir explicitamente uma pasta de recebimento. 
    
- Em _lppEntryID_, o identificador de entrada da pasta de recebimento para a classe base apontado pelo parâmetro _lppszExplicitClass_ . 
    
Por exemplo, suponha que a pasta de recebimento da classe de mensagem **IPM. Observação** tiver sido definida para a entrada identificador da caixa de entrada e **GetReceiveFolder** é chamado com o conteúdo de _lpszMessageClass_ definida como **IPM. Note.Phone**. Se **IPM. Note.Phone** não têm um explícitas recebe conjunto de pastas, **GetReceiveFolder** retorna o identificador de entrada da caixa de entrada no _lppEntryID_ e **IPM. Observação** em _lppszExplicitClass_.
  
Se o cliente chama **GetReceiveFolder** para uma classe de mensagem e não tiver definido uma pasta de recebimento para essa classe de mensagem, _lppszExplicitClass_ é uma cadeia de caracteres de comprimento zero, uma cadeia de caracteres em formato Unicode ou uma cadeia de caracteres, no formato ANSI dependendo se o cliente definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ . 
  
Um padrão receber pasta, obtida passando NULL no parâmetro _lpszMessageClass_ , sempre existe para cada armazenamento de mensagens. 
  
Um cliente deve chamar a função [MAPIFreeBuffer](mapifreebuffer.md) quando isso é feito com o identificador de entrada retornado em _lppEntryID_ liberar a memória que contém esse identificador de entrada. Ele também deve chamar **MAPIFreeBuffer** quando isso é feito com a cadeia de caracteres de classe de mensagem retornada em _lppszExplicitClass_ liberar a memória que contém a cadeia de caracteres. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI usa o método **IMsgStore::GetReceiveFolder** para localizar a pasta de caixa de entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

