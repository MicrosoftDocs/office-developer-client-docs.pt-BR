---
title: Desligar a um provedor de serviços
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 71706fc970170f74aa5555da29d904c08c0422f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770411"
---
# <a name="shutting-down-a-service-provider"></a>Desligar a um provedor de serviços

 
  
**Aplica-se a**: Outlook 
  
Quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) terminar a sessão e desligue todos os provedores de serviço ativo, MAPI por sua vez chama os métodos a seguir: 
  
- [IABLogon::Logoff](iablogon-logoff.md) para provedores de catálogo de endereços. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) para provedores de armazenamento de mensagem. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) para provedores de transporte. 
    
Esses métodos têm implementações semelhantes. As principais tarefas que está executando um método logoff são:
  
- Liberar todos os objetos abertos, incluindo subobjetos e objetos de status.
    
- Chamando o suporte ao método do objeto [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para diminuir sua contagem de referência. 
    
- Removendo todas as estruturas [MAPIUID](mapiuid.md) registradas do seu provedor. 
    
- Removendo a linha do seu provedor na tabela de status.
    
- Execução de tarefas relacionadas ao limpando recursos, como o seguinte:
    
  - Encerrando uma conexão com um servidor remoto.
    
  - A referência de diminuição contar com o objeto de logon.
    
  - Removendo o objeto de logon da lista de objetos de logon que armazena seu provedor.
    
  - No modo de depuração, emitindo rastreamentos para localizar os objetos que têm vazamento de memória.
    
Quando seu método logoff retorna, MAPI chama o seguinte:
  
- Método de **IUnknown:: Release** do objeto seu logon. 
    
- Método de **desligamento** do objeto do provedor para executar quaisquer tarefas de limpeza final. Dependendo do tipo do seu provedor, é chamado um dos métodos a seguir: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) para provedores de catálogo de endereços 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) para provedores de armazenamento de mensagem 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) para provedores de transporte 
    
- Método de **IUnknown:: Release** do objeto do provedor. 
    
Se seu provedor for um armazenamento de mensagens, uma chamada de cliente para [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) também iniciará o processo de desligamento. **StoreLogoff** desliga o provedor de armazenamento de uma determinada mensagem e não tem efeito sobre a sessão. Apenas um provedor de armazenamento de mensagens pode ser desligado com este método; Não há explícito para serem desligados um provedor de transporte ou catálogo determinado endereço. Para obter informações sobre como responder a um **StoreLogoff** chamada, consulte [Sendo para baixo uma mensagem de provedor de armazenamento](shutting-down-a-message-store-provider.md).
  
DLL do seu provedor será descarregado quando a função de API do Win32 **FreeLibrary**, uma chamada feita após o último cliente ativo tiver chamado [MAPIUninitialize](mapiuninitialize.md)chamadas de MAPI. Neste momento, seu provedor de serviços serão terminar desligado. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

