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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348773"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém a pasta que foi estabelecida como o destino para mensagens de entrada de uma classe de mensagem especificada ou como a pasta de recebimento padrão para o repositório de mensagens.
  
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
  
> no Um ponteiro para uma classe de mensagem associada a uma pasta de recebimento. Se o parâmetro _lpszMessageClass_ estiver definido como nulo ou uma cadeia de caracteres vazia, **GetReceiveFolder** retornará a pasta de recebimento padrão para o repositório de mensagens. 
    
 _ulFlags_
  
> no Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas e retornadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> A cadeia de caracteres da classe da mensagem está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres da classe da mensagem estará no formato ANSI.
    
 _lpcbEntryID_
  
> bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> bota Um ponteiro para um ponteiro para o identificador de entrada da pasta receber solicitada.
    
 _lppszExplicitClass_
  
> bota Um ponteiro para um ponteiro para a classe de mensagem que define explicitamente como sua pasta receber a pasta apontada pelo _lppEntryID_. Essa classe de mensagem deve ser igual à classe no parâmetro _lpszMessageClass_ ou a uma classe base dessa classe. Passar NULL indica que a pasta apontada por _lppEntryID_ é a pasta de recebimento padrão para o repositório de mensagens. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta de recebimento foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: GetReceiveFolder** Obtém o identificador de entrada de uma pasta de recebimento, uma pasta designada para receber mensagens de entrada de uma determinada classe de mensagem. Os chamadores podem especificar uma classe de mensagem ou nulo no parâmetro _lpszMessageClass_ . Se _lpszMessageClass_ for nulo, **GetReceiveFolder** retornará os seguintes valores: 
  
- No _lppszExplicitClass_, o nome da primeira classe base da classe de mensagem apontada por _lpszMessageClass_ que define explicitamente uma pasta de recebimento. 
    
- No _lppEntryID_, o identificador de entrada da pasta de recebimento da classe base indicada pelo parâmetro _lppszExplicitClass_ . 
    
Por exemplo, suponha a pasta de recebimento da classe de mensagem **IPM. A observação** foi definida como o identificador de entrada da caixa de entrada e **GetReceiveFolder** é chamado com o conteúdo de _lpszMessageClass_ definido como **IPM. Note. Phone**. Se **IPM. Note. o telefone** não tem um conjunto de pastas de recebimento explícito, **GetReceiveFolder** retorna o identificador de entrada da caixa de entrada no _lppEntryID_ e **IPM. Nota** no _lppszExplicitClass_.
  
Se o cliente chama **GetReceiveFolder** para uma classe de mensagem e não definiu uma pasta de recebimento para essa classe de mensagem, _lppszExplicitClass_ é uma cadeia de comprimento zero, uma cadeia de caracteres no formato Unicode ou uma cadeia de caracteres no formato ANSI, dependendo se o cliente define o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ . 
  
Uma pasta de recebimento padrão, obtida passando NULL no parâmetro _lpszMessageClass_ , sempre existe para cada repositório de mensagens. 
  
Um cliente deve chamar a função [MAPIFreeBuffer](mapifreebuffer.md) quando ele é feito com o identificador de entrada retornado em _lppEntryID_ para liberar a memória que contém esse identificador de entrada. Ele também deve chamar **MAPIFreeBuffer** quando ele é feito com a cadeia de caracteres de classe de mensagem retornada no _lppszExplicitClass_ para liberar a memória que retém essa cadeia de caracteres. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetInbox  <br/> |MFCMAPI usa o método **IMsgStore:: GetReceiveFolder** para localizar a pasta caixa de entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

