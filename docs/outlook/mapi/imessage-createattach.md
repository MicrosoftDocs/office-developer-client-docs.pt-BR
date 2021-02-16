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
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417665"
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
  
> [in] Ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a mensagem. Passar resultados NULL na interface padrão da mensagem ou **IMessage**, sendo retornado. 
    
 _ulFlags_
  
> [in] Bitmask de sinalizadores que controla como o anexo é criado. O sinalizador a seguir pode ser definido:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **CreateAttach** retorne com êxito, possivelmente antes que o anexo seja totalmente acessível para o cliente de chamada. Se o anexo não estiver acessível, fazer uma chamada subsequente pode resultar em um erro. 
    
 _lpulAttachmentNum_
  
> [out] Ponteiro para um número de índice que identifica o anexo recém-criado. Esse número é válido somente quando a mensagem está aberta e é a base para a propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.
    
 _lppAttach_
  
> [out] Ponteiro para um ponteiro para o objeto de anexo aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O anexo foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMessage::CreateAttach** cria um novo anexo em uma mensagem. O novo anexo e todas as propriedades definidas para ele não estarão disponíveis até que um cliente tenha chamado o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do anexo e o método **IMAPIProp::SaveChanges** da mensagem. 
  
O número do anexo apontado por  _lpulAttachmentNum_ é exclusivo e válido somente no contexto da mensagem. Ou seja, dois anexos em duas mensagens diferentes podem ter o mesmo número, enquanto dois anexos na mesma mensagem não podem. 
  
## <a name="see-also"></a>Confira também



[IMessage : IMAPIProp](imessageimapiprop.md)

