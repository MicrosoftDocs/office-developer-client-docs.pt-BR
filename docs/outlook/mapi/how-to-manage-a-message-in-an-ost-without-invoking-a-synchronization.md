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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="25065-103">Gerenciar mensagens no OST sem chamar uma sincronização no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="25065-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="25065-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25065-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25065-105">Este tópico contém um exemplo de código em C++ que mostra como usar `IID_IMessageRaw` em **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obter uma interface **[IMessage](imessageimapiprop.md)** que gerencia uma mensagem em um arquivo de pastas offline (OST) sem forçar um download do todo mensagem quando o cliente está no modo cache do Exchange.</span><span class="sxs-lookup"><span data-stu-id="25065-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="25065-106">Quando um cliente está no modo cache do Exchange, mensagens em OST podem estar em um dos dois estados:</span><span class="sxs-lookup"><span data-stu-id="25065-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="25065-107">Toda a mensagem que contém o cabeçalho e corpo é baixada.</span><span class="sxs-lookup"><span data-stu-id="25065-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="25065-108">A mensagem com apenas seu cabeçalho é baixada.</span><span class="sxs-lookup"><span data-stu-id="25065-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="25065-109">Quando você solicitar uma interface **IMessage** para uma mensagem em um OST e o cliente está no modo cache do Exchange, use `IID_IMessageRaw`.</span><span class="sxs-lookup"><span data-stu-id="25065-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="25065-110">Se você usar `IID_IMessage` para solicitar uma interface **IMessage** , e se a mensagem tiver apenas seu cabeçalho baixado em OST, você chama uma sincronização que tenta fazer o download de toda a mensagem.</span><span class="sxs-lookup"><span data-stu-id="25065-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="25065-111">Se você usar `IID_IMessageRaw` ou `IID_IMessage` para solicitar uma interface **IMessage** , as interfaces que são retornadas são idênticas em uso.</span><span class="sxs-lookup"><span data-stu-id="25065-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="25065-112">A interface de **IMessage** que foi solicitada usando `IID_IMessageRaw` retornará uma mensagem de email enquanto ele existe no OST e sincronização não está sendo forçada.</span><span class="sxs-lookup"><span data-stu-id="25065-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="25065-113">O exemplo a seguir mostra como chamar o método **OpenEntry** , passando `IID_IMessageRaw` em vez de `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="25065-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="25065-114">Se o método **OpenEntry** retorna o código de erro **MAPI_E_INTERFACE_NOT_SUPPORTED** , indica que o armazenamento de mensagens não oferece suporte ao acessar a mensagem no modo raw.</span><span class="sxs-lookup"><span data-stu-id="25065-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="25065-115">Nessa situação, tente o método **OpenEntry** novamente ao passar `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="25065-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="25065-116">`IID_IMessageRaw`não podem ser definidos no arquivo de cabeçalho para download que você possui atualmente.</span><span class="sxs-lookup"><span data-stu-id="25065-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="25065-117">Nesse caso, você pode adicioná-la ao seu código usando a seguinte definição.</span><span class="sxs-lookup"><span data-stu-id="25065-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="25065-118">Use a macro DEFINE_OLEGUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar o nome simbólico do GUID a seu valor.</span><span class="sxs-lookup"><span data-stu-id="25065-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="25065-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="25065-119">See also</span></span>

- [<span data-ttu-id="25065-120">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="25065-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="25065-121">Acessar um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="25065-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="25065-122">Abrir um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="25065-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

