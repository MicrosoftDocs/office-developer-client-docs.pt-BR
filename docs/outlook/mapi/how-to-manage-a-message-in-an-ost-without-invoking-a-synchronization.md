---
title: Gerenciar mensagens no OST sem chamar uma sincronização no modo cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contém um exemplo de código em C++ que mostra como usar IID_IMessageRaw no IMsgStore::OpenEntry para obter uma interface IMessage que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar um download de toda a mensagem quando o cliente esteja em cache do Exchange Modo.
ms.openlocfilehash: f094f5a7deae705ed64b912483726aeb409fb107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568102"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Gerenciar mensagens no OST sem chamar uma sincronização no modo cache do Exchange

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo de código em C++ que mostra como usar `IID_IMessageRaw` em **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obter uma interface **[IMessage](imessageimapiprop.md)** que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar um download do todo mensagem quando o cliente está no modo cache do Exchange. 
  
Quando um cliente está no modo cache do Exchange, mensagens em OST podem estar em um dos dois estados:
  
- Toda a mensagem que contém o cabeçalho e corpo é baixada.
    
- A mensagem com apenas seu cabeçalho é baixada.
    
Quando você solicitar uma interface **IMessage** para uma mensagem em um OST e o cliente está no modo cache do Exchange, use `IID_IMessageRaw`. Se você usar `IID_IMessage` para solicitar uma interface **IMessage** , e se a mensagem tiver apenas seu cabeçalho baixado em OST, você chama uma sincronização que tenta fazer o download de toda a mensagem. 
  
Se você usar `IID_IMessageRaw` ou `IID_IMessage` para solicitar uma interface **IMessage** , as interfaces que são retornadas são idênticas em uso. A interface de **IMessage** que foi solicitada usando `IID_IMessageRaw` retornará uma mensagem de email enquanto ele existe no OST e sincronização não está sendo forçada. 
  
O exemplo a seguir mostra como chamar o método **OpenEntry** , passando `IID_IMessageRaw` em vez de `IID_IMessage`.
  
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

Se o método **OpenEntry** retorna o código de erro **MAPI_E_INTERFACE_NOT_SUPPORTED** , indica que o armazenamento de mensagens não oferece suporte ao acessar a mensagem no modo raw. Nessa situação, tente o método **OpenEntry** novamente ao passar `IID_IMessage`.

> [!IMPORTANT]
>  `IID_IMessageRaw`não podem ser definidos no arquivo de cabeçalho para download que você possui atualmente. Nesse caso, você pode adicioná-la ao seu código usando a seguinte definição. Use a macro DEFINE_OLEGUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar o nome simbólico do GUID a seu valor. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Confira também

- [Sobre as adições de MAPI](about-mapi-additions.md) 
- [Acessar um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

