---
title: Gerenciar mensagens no OST sem invocar uma sincronização no modo cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'Contém um exemplo de código em C++ que mostra como usar o IID_IMessageRaw no IMsgStore:: OpenEntry para obter uma interface IMessage que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar um download de toda a mensagem quando o cliente está no Exchange em cache Mode.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418754"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Gerenciar mensagens no OST sem invocar uma sincronização no modo cache do Exchange

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo de código em C++ que mostra como usar `IID_IMessageRaw` o **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** para obter uma interface do **[IMessage](imessageimapiprop.md)** que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar o download de toda a mensagem quando o cliente está no modo cache do Exchange. 
  
Quando um cliente está no modo cache do Exchange, as mensagens no OST podem estar em um dos dois Estados:
  
- Toda a mensagem que contém o cabeçalho e o corpo é baixada.
    
- A mensagem com apenas seu cabeçalho é baixada.
    
Quando você solicita uma interface **IMessage** para uma mensagem em um Ost e o cliente está no modo cache do Exchange, use `IID_IMessageRaw`. Se você usar `IID_IMessage` o para solicitar uma interface do **IMessage** e se a mensagem tiver apenas seu cabeçalho baixado no OST, você invocará uma sincronização que tenta baixar toda a mensagem. 
  
Se você usar `IID_IMessageRaw` ou `IID_IMessage` para solicitar uma interface **IMessage** , as interfaces que são retornadas são idênticas em uso. A interface **IMessage** que foi solicitada usando `IID_IMessageRaw` retorna uma mensagem de email como ela existe no Ost e a sincronização não é forçada. 
  
O exemplo a seguir mostra como chamar o método **OpenEntry** , passando `IID_IMessageRaw` em vez `IID_IMessage`de.
  
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

Se o método **OpenEntry** retornar o código de erro **MAPI_E_INTERFACE_NOT_SUPPORTED** , ele indica que o repositório de mensagens não oferece suporte ao acesso à mensagem no modo bruto. Nessa situação, tente o método **OpenEntry** novamente transmitindo `IID_IMessage`.

> [!IMPORTANT]
>  `IID_IMessageRaw`Não pode ser definido no arquivo de cabeçalho baixável que você tem no momento. Nesse caso, você pode adicioná-lo ao seu código usando a definição a seguir. Use a macro DEFINE_OLEGUID definida no arquivo de cabeçalho do Microsoft Windows Software Development Kit (SDK) guiddef. h para associar o nome simbólico GUID a seu valor. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Confira também

- [Sobre as adições de MAPI](about-mapi-additions.md) 
- [Acessar o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

