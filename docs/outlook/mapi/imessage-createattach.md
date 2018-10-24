---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572079"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um novo anexo.
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> [in] Ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a mensagem. Passagem nula resulta em interface padrão ou **IMessage**, a mensagem que está sendo retornada. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla como o anexo é criado. O seguinte sinalizador pode ser definido:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **CreateAttach** retornar com êxito, possivelmente antes que o anexo seja totalmente acessível para o cliente da chamada. Se o anexo não está acessível, fazendo uma chamada subsequente a ele pode resultar em um erro. 
    
 _lpulAttachmentNum_
  
> [out] Ponteiro para um número de índice que identifica o anexo recém-criado. Esse número é válido somente quando a mensagem é aberta e é a base para a propriedade de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.
    
 _lppAttach_
  
> [out] Ponteiro para um ponteiro para o objeto de abrir anexo.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O anexo foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMessage::CreateAttach** cria um novo anexo em uma mensagem. O novo anexo e as propriedades que são definidas para ele, não estão disponíveis até que um cliente tenha chamado o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do anexo e o método de **IMAPIProp::SaveChanges** da mensagem. 
  
O número de anexo apontado pela _lpulAttachmentNum_ é exclusivo e válido somente dentro do contexto da mensagem. Ou seja, dois anexos em duas mensagens diferentes podem ter o mesmo número enquanto dois anexos na mesma mensagem não é possível. 
  
## <a name="see-also"></a>Confira também



[IMessage : IMAPIProp](imessageimapiprop.md)

