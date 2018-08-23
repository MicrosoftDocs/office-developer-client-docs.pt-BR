---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 48df5362106e849f061b0797736fad82fafa6584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588710"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um anexo. 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parâmetros

 _ulAttachmentNum_
  
> [in] Número de índice do anexo seja aberto, conforme armazenado na propriedade de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo. Esse número de índice exclusivamente identifica o anexo na mensagem e é válido apenas no contexto da mensagem.
    
 _lpInterface_
  
> [in] Ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o anexo. Passagem nula resulta na interface padrão do anexo ou **IAttach**, sendo retornados. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla como o anexo é aberto. Sinalizadores a seguir podem ser definidos: 
    
MAPI_BEST_ACCESS 
  
> Solicita que o anexo seja aberto com as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo. Por exemplo, se o cliente tem a permissão de leitura/gravação, o anexo deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver acesso somente leitura, o anexo deve ser aberto com acesso somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenAttach** retornar com êxito, possivelmente antes que o anexo seja totalmente disponível para o cliente da chamada. Se o anexo não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, anexos abertos com acesso somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
 _lppAttach_
  
> [out] Ponteiro para um ponteiro para abrir o anexo.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O anexo foi aberto com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMessage::OpenAttach** abre o anexo da mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para abrir um anexo, você deve ter acesso ao seu número de anexos ou a propriedade **PR_ATTACH_NUM** . Chame [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) para recuperar a tabela de anexos da mensagem e localize a linha que representa o anexo a ser aberto. Para obter mais informações, consulte [abertura de um anexo](opening-an-attachment.md) . 
  
Não tente abrir um anexo várias vezes; os resultados são indefinido e dependentes de provedor de armazenamento de mensagem.
  
Você pode solicitar que o anexo seja aberto no modo de leitura/gravação, em vez do modo padrão de somente leitura. No entanto, se o anexo realmente será aberto no modo leitura/gravação é do provedor de repositório de mensagem. Você pode tentar modificar o anexo, preparando para lidar com falhas ou marque o nível de acesso que foi concedido Recuperando a propriedade de **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) do anexo, se ele estiver disponível. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp usado para  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI usa o método **IMessage::OpenAttach** para abrir a objetos de anexo  <br/> |
   
## <a name="see-also"></a>Confira também



[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

