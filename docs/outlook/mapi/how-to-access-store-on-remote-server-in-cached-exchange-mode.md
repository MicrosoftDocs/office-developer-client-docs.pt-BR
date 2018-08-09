---
title: Acessar um repositório no servidor remoto, quando o Outlook estiver no modo cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Modificado pela última vez: 02 de julho de 2012'
ms.openlocfilehash: 8f1afd31f017b73fa5270d8fbf4c2a1c8fa08880
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766725"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Acessar um repositório no servidor remoto, quando o Outlook estiver no modo cache do Exchange
 
**Aplica-se a**: Outlook 
  
Este tópico contém um exemplo de código em C++ que mostra como usar o sinalizador **MAPI_NO_CACHE** para abrir uma pasta ou uma mensagem em um armazenamento de mensagens no servidor remoto, quando o Microsoft Office Outlook está no modo cache do Exchange. 
  
Modo cache do Exchange permite que o Outlook para usar uma cópia local da caixa de correio de um usuário com o Outlook mantém uma conexão on-line para uma cópia remota da caixa de correio do usuário no servidor Exchange remoto. Quando o Outlook está em execução no modo cache do Exchange, por padrão, qualquer soluções MAPI que faça logon mesma sessão também estão conectadas ao repositório de mensagens armazenadas em cache. Todos os dados que são acessados e quaisquer alterações que são feitas são feitas em relação a cópia local da caixa de correio.
  
Um provedor de cliente ou serviço pode substituir a conexão ao repositório de mensagem local e abrir uma mensagem ou uma pasta no repositório remoto definindo o bit para **MAPI_NO_CACHE** no parâmetro *ulFlags* ao chamar **[IMsgStore::OpenEntry](imsgstore-openentry.md)**. 
  
O exemplo de código a seguir mostra como chamar **IMsgStore::OpenEntry** com o sinalizador **MAPI_NO_CACHE** definido no parâmetro *ulFlags* para abrir a pasta raiz no armazenamento de mensagens remoto. 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

Se você abriu o armazenamento de mensagens com o sinalizador **MDB_ONLINE** no servidor remoto, você não precisará usar o sinalizador **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>Confira também

- [Sobre as adições de MAPI](about-mapi-additions.md)
- [Abrir um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gerenciar mensagens em um OST sem solicitar uma sincronização do modo cache do Exchange](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

