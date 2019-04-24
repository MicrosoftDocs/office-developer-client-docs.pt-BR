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
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349249"
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
  
> no Número de índice do anexo a ser aberto, conforme armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo. Esse número de índice identifica exclusivamente o anexo na mensagem e é válido somente no contexto da mensagem.
    
 _lpInterface_
  
> no Ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o anexo. Passar resultados nulos na interface padrão do anexo ou **IAttach**, sendo retornado. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores que controla como o anexo é aberto. Os seguintes sinalizadores podem ser definidos: 
    
MAPI_BEST_ACCESS 
  
> Solicita que o anexo seja aberto com as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo. Por exemplo, se o cliente tiver permissão de leitura/gravação, o anexo deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver acesso somente leitura, o anexo deverá ser aberto com acesso somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenAttach** seja retornado com êxito, possivelmente antes que o anexo esteja totalmente disponível para o cliente de chamada. Se o anexo não estiver disponível, fazer uma chamada subsequente para ele pode causar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os anexos são abertos com acesso somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida. 
    
 _lppAttach_
  
> bota Ponteiro para um ponteiro para o anexo aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O anexo foi aberto com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMessage:: OpenAttach** abre o anexo de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para abrir um anexo, você deve ter acesso ao número de anexo ou à propriedade **PR_ATTACH_NUM** . Chame [IMessage::](imessage-getattachmenttable.md) GetAttachmentTable para recuperar a tabela de anexos da mensagem e localizar a linha que representa o anexo a ser aberto. ConFira como [abrir um anexo](opening-an-attachment.md) para obter mais informações. 
  
Não tente abrir um anexo várias vezes; os resultados são indefinidos e dependentes do provedor de armazenamento de mensagens.
  
Você pode solicitar que o anexo seja aberto no modo de leitura/gravação, em vez do modo somente leitura padrão. No enTanto, se o anexo será realmente aberto no modo de leitura/gravação está no provedor de armazenamento de mensagens. Você pode tentar modificar o anexo, se preparar para lidar com uma possível falha ou verificar o nível de acesso que foi concedido ao recuperar a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) do anexo, se estiver disponível. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp usado para  <br/> |CAttachmentsDlg:: OpenItemProp  <br/> |MFCMAPI usa o método **IMessage:: OpenAttach** para abrir objetos Attachment,  <br/> |
   
## <a name="see-also"></a>Confira também



[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

