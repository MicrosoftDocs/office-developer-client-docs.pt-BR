---
title: Desligar um provedor de serviços
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339204"
---
# <a name="shutting-down-a-service-provider"></a>Desligar um provedor de serviços

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) para encerrar a sessão e desligar todos os provedores de serviços ativos, o MAPI, por sua vez, chama os seguintes métodos: 
  
- [IABLogon::Logoff para](iablogon-logoff.md) provedores de agendamento de endereços. 
    
- [IMSLogon::Logoff para](imslogon-logoff.md) provedores de armazenamento de mensagens. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) para provedores de transporte. 
    
Esses métodos têm implementações semelhantes. As principais tarefas que um método logoff executa são as seguinte:
  
- Liberação de todos os objetos abertos, incluindo subobjetos e objetos de status.
    
- Chamar o método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do objeto de suporte para rebaixar sua contagem de referência. 
    
- Removendo todas as estruturas [MAPIUID](mapiuid.md) registradas do provedor. 
    
- Removendo a linha do provedor na tabela de status.
    
- Executar tarefas relacionadas à limpeza de recursos, como as seguintes:
    
  - Terminando uma conexão com um servidor remoto.
    
  - Diminuindo a contagem de referência no objeto de logon.
    
  - Removendo o objeto de logon da lista de objetos de logon que seu provedor armazena.
    
  - No modo de depuração, emita rastreamentos para localizar objetos que tenham vazado memória.
    
Quando o método logoff retorna, o MAPI chama o seguinte:
  
- Método **IUnknown::Release** do objeto de logon. 
    
- O método Shutdown do objeto **do** provedor para executar qualquer tarefa de limpeza final. Dependendo do tipo de provedor, um dos seguintes métodos é chamado: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) para provedores de agendas 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) para provedores de armazenamento de mensagens 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) para provedores de transporte 
    
- Método **IUnknown::Release do seu** objeto provedor. 
    
Se o provedor for um repositório de mensagens, uma chamada de cliente para [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) também iniciará o processo de desligamento. **StoreLogoff** desliga um provedor de armazenamento de mensagens específico e não tem efeito na sessão. Somente um provedor de armazenamento de mensagens pode ser desligado com esse método; não há uma maneira explícita de desligar um determinado address book ou provedor de transporte. Para obter informações sobre como responder a uma **chamada StoreLogoff,** consulte [Desligar um Provedor de Armazenamento de Mensagens.](shutting-down-a-message-store-provider.md)
  
A DLL do seu provedor será descarregada quando MAPI chamar a função de API **Win32 FreeLibrary**, uma chamada que é feita após o último cliente ativo ter chamado [MAPIUninitialize](mapiuninitialize.md). Neste momento, seu provedor de serviços terá terminado de desligar. 
  
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

