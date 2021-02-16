---
title: Acessar um armazenamento no servidor remoto quando o Outlook estiver no Modo Cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420728"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Acessar um armazenamento no servidor remoto quando o Outlook estiver no Modo Cache do Exchange
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém um exemplo de código em C++ que mostra como usar o sinalizador **MAPI_NO_CACHE** para abrir uma pasta ou uma mensagem em um armazenamento de mensagens no servidor remoto quando o Microsoft Office Outlook está no Modo Cache do Exchange. 
  
O Modo Cache do Exchange permite que o Outlook use uma cópia local da caixa de correio de um usuário enquanto o Outlook mantém uma conexão online com uma cópia remota da caixa de correio do usuário no servidor Exchange remoto. Quando o Outlook está sendo executado no Modo Cache do Exchange, por padrão, todas as soluções MAPI que fazem logon na mesma sessão também são conectadas ao armazenamento de mensagens em cache. Todos os dados acessados e quaisquer alterações feitas serão feitas na cópia local da caixa de correio.
  
Um cliente ou provedor de serviços pode substituir a conexão com o repositório de mensagens local e abrir uma mensagem ou uma pasta no repositório remoto definindo o bit para **MAPI_NO_CACHE** no  *parâmetro ulFlags*  ao chamar **[IMsgStore::OpenEntry](imsgstore-openentry.md)**. 
  
O exemplo de código a seguir mostra como chamar **IMsgStore::OpenEntry** com o sinalizador MAPI_NO_CACHE definido no parâmetro *ulFlags* para abrir **a** pasta raiz no repositório de mensagens remoto. 
  
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

Se você abriu o armazenamento de mensagens **com o sinalizador MDB_ONLINE** no servidor remoto, não será preciso usar o sinalizador **MAPI_NO_CACHE** mensagem. 
  
## <a name="see-also"></a>Confira também

- [Sobre as adições de MAPI](about-mapi-additions.md)
- [Abrir o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gerenciar mensagens em um OST sem solicitar uma sincronização do modo cache do Exchange](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

