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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405895"
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
  
> [in] Número de índice do anexo a ser aberto, conforme armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo. Esse número de índice identifica exclusivamente o anexo na mensagem e é válido somente no contexto da mensagem.
    
 _lpInterface_
  
> [in] Ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o anexo. Passar resultados NULL na interface padrão do anexo ou **IAttach** está sendo retornado. 
    
 _ulFlags_
  
> [in] Máscara de bits de sinalizadores que controla como o anexo é aberto. Os sinalizadores a seguir podem ser definidos: 
    
MAPI_BEST_ACCESS 
  
> Solicita que o anexo seja aberto com as permissões máximas de rede permitidas para o usuário e o acesso máximo ao aplicativo cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o anexo deverá ser aberto com permissão de leitura/gravação; se o cliente tiver acesso somente leitura, o anexo deverá ser aberto com acesso somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenAttach** retorne com êxito, possivelmente antes do anexo estar totalmente disponível para o cliente de chamada. Se o anexo não estiver disponível, fazer uma chamada subsequente pode causar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os anexos são abertos com acesso somente leitura, e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida. 
    
 _lppAttach_
  
> [out] Ponteiro para um ponteiro para o anexo aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O anexo foi aberto com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMessage::OpenAttach** abre o anexo de uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para abrir um anexo, você deve ter acesso ao seu número de anexo **ou PR_ATTACH_NUM** propriedade. Chame [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) para recuperar a tabela de anexos da mensagem e localizar a linha que representa o anexo a ser aberto. Consulte [Abrir um anexo](opening-an-attachment.md) para obter mais informações. 
  
Não tente abrir um anexo várias vezes; os resultados são indefinido e dependem do provedor do armazenamento de mensagens.
  
Você pode solicitar que o anexo seja aberto no modo de leitura/gravação, em vez do modo padrão somente leitura. No entanto, o provedor de armazenamento de mensagens decidirá se o anexo será realmente aberto no modo de leitura/gravação. Você pode tentar modificar o anexo, preparar-se para lidar com uma possível falha ou verificar o nível de acesso concedido pela recuperação da propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md)do anexo, se ele estiver disponível. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp Usado para  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI usa o **método IMessage::OpenAttach** para abrir objetos attachment,  <br/> |
   
## <a name="see-also"></a>Confira também



[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

