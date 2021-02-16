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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="7ab12-103">Gerenciar mensagens no OST sem invocar uma sincronização no modo Cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="7ab12-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="7ab12-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ab12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ab12-105">Este tópico contém um exemplo de código em C++ que mostra como usar em `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obter uma interface **[IMessage](imessageimapiprop.md)** que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar um download da mensagem inteira quando o cliente está no Modo Cache do Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ab12-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="7ab12-106">Quando um cliente está no Modo Cache do Exchange, as mensagens no OST podem estar em um dos dois estados:</span><span class="sxs-lookup"><span data-stu-id="7ab12-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="7ab12-107">A mensagem inteira que contém o header e o corpo é baixada.</span><span class="sxs-lookup"><span data-stu-id="7ab12-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="7ab12-108">A mensagem com apenas seu header é baixada.</span><span class="sxs-lookup"><span data-stu-id="7ab12-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="7ab12-109">Quando você solicitar uma interface **IMessage** para uma mensagem em um OST e o cliente estiver no Modo Cache do Exchange, use  `IID_IMessageRaw` .</span><span class="sxs-lookup"><span data-stu-id="7ab12-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="7ab12-110">Se você usar para solicitar uma  `IID_IMessage` interface **IMessage** e se a mensagem tiver apenas seu header baixado no OST, você invocará uma sincronização que tentará baixar a mensagem inteira.</span><span class="sxs-lookup"><span data-stu-id="7ab12-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="7ab12-111">Se você usar  `IID_IMessageRaw` ou solicitar uma interface  `IID_IMessage` **IMessage,** as interfaces retornadas serão idênticas em uso.</span><span class="sxs-lookup"><span data-stu-id="7ab12-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="7ab12-112">A interface **IMessage** que foi solicitada usando retorna uma mensagem de email como ela existe no OST, e a sincronização  `IID_IMessageRaw` não é forçada.</span><span class="sxs-lookup"><span data-stu-id="7ab12-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="7ab12-113">O exemplo a seguir mostra como chamar o **método OpenEntry,** passando  `IID_IMessageRaw` em vez de  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="7ab12-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="7ab12-114">Se o **método OpenEntry** retornar o **MAPI_E_INTERFACE_NOT_SUPPORTED** código de erro, ele indicará que o armazenamento de mensagens não dá suporte ao acesso à mensagem no modo bruto.</span><span class="sxs-lookup"><span data-stu-id="7ab12-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="7ab12-115">Nessa situação, tente o **método OpenEntry** novamente passando  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="7ab12-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="7ab12-116">`IID_IMessageRaw` talvez não seja definido no arquivo de header baixável que você tem no momento.</span><span class="sxs-lookup"><span data-stu-id="7ab12-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="7ab12-117">Nesse caso, você pode adicioná-lo ao seu código usando a definição a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ab12-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="7ab12-118">Use a DEFINE_OLEGUID macro definida no arquivo de título guiddef.h do Microsoft Software Development Kit do Windows (SDK do Windows) para associar o nome simbólico guid ao seu valor.</span><span class="sxs-lookup"><span data-stu-id="7ab12-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="7ab12-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ab12-119">See also</span></span>

- [<span data-ttu-id="7ab12-120">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="7ab12-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="7ab12-121">Acessar o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="7ab12-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="7ab12-122">Abrir o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="7ab12-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

