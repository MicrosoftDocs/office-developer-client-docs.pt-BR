---
title: Gerenciar mensagens no OST sem invocar uma sincronização no modo Cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contém um exemplo de código em C++ que mostra como usar o IID_IMessageRaw em IMsgStore::OpenEntry para obter uma interface IMessage que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar um download da mensagem inteira quando o cliente está no Modo Cache do Exchange.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418754"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Gerenciar mensagens no OST sem invocar uma sincronização no modo Cache do Exchange

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo de código em C++ que mostra como usar em `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obter uma interface **[IMessage](imessageimapiprop.md)** que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar um download da mensagem inteira quando o cliente está no Modo Cache do Exchange. 
  
Quando um cliente está no Modo Cache do Exchange, as mensagens no OST podem estar em um dos dois estados:
  
- A mensagem inteira que contém o header e o corpo é baixada.
    
- A mensagem com apenas seu header é baixada.
    
Quando você solicitar uma interface **IMessage** para uma mensagem em um OST e o cliente estiver no Modo Cache do Exchange, use  `IID_IMessageRaw` . Se você usar para solicitar uma  `IID_IMessage` interface **IMessage** e se a mensagem tiver apenas seu header baixado no OST, você invocará uma sincronização que tentará baixar a mensagem inteira. 
  
Se você usar  `IID_IMessageRaw` ou solicitar uma interface  `IID_IMessage` **IMessage,** as interfaces retornadas serão idênticas em uso. A interface **IMessage** que foi solicitada usando retorna uma mensagem de email como ela existe no OST, e a sincronização  `IID_IMessageRaw` não é forçada. 
  
O exemplo a seguir mostra como chamar o **método OpenEntry,** passando  `IID_IMessageRaw` em vez de  `IID_IMessage` .
  
```cpp
HRESULT HrOpenRawMessage ( 
    LPMDB lpMSB,  
    ULONG cbEntryID,  
    LPENTRYID lpEntryID,  
    ULONG ulFlags,  
    LPMESSAGE* lpMessage) 
{ 
    ULONG ulObjType = NULL; 
 
    HRESULT hRes = lpMDB->OpenEntry( 
        cbEntryID, 
        lpEntryID, 
        IID_IMessageRaw, 
        ulFlags, 
        &ulObjType, 
        (LPUNKNOWN*) lpMessage)); 
 
   return hRes; 
} 

```

Se o **método OpenEntry** retornar o **MAPI_E_INTERFACE_NOT_SUPPORTED** código de erro, ele indicará que o armazenamento de mensagens não dá suporte ao acesso à mensagem no modo bruto. Nessa situação, tente o **método OpenEntry** novamente passando  `IID_IMessage` .

> [!IMPORTANT]
>  `IID_IMessageRaw` talvez não seja definido no arquivo de header baixável que você tem no momento. Nesse caso, você pode adicioná-lo ao seu código usando a definição a seguir. Use a DEFINE_OLEGUID macro definida no arquivo de título guiddef.h do Microsoft Software Development Kit do Windows (SDK do Windows) para associar o nome simbólico guid ao seu valor. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Confira também

- [Sobre as adições de MAPI](about-mapi-additions.md) 
- [Acessar o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

