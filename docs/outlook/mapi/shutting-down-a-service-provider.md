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
  
Quando um cliente chama o método [IMAPISession:: logoff](imapisession-logoff.md) para finalizar a sessão e desligar todos os provedores de serviços ativos, MAPI por vez chama os seguintes métodos: 
  
- [IABLogon:: fazer logoff](iablogon-logoff.md) para provedores de catálogo de endereços. 
    
- [IMSLogon:: fazer logoff](imslogon-logoff.md) para provedores de repositórios de mensagens. 
    
- [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) para provedores de transporte. 
    
Esses métodos têm implementações semelhantes. As principais tarefas executadas por um método de logoff são as seguintes:
  
- Liberar todos os objetos abertos, incluindo subobjetos e objetos de status.
    
- Chamar o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do objeto support para decrementar sua contagem de referência. 
    
- Removendo todas as estruturas [MAPIUID](mapiuid.md) registradas do provedor. 
    
- Removendo a linha do provedor na tabela status.
    
- Executar qualquer tarefa relacionada à limpeza de recursos, como o seguinte:
    
  - Encerrar uma conexão com um servidor remoto.
    
  - Decrementar a contagem de referência no objeto de logon.
    
  - Remover o objeto de logon da lista de objetos de logon que seu provedor armazena.
    
  - No modo de depuração, emitir rastreamentos para localizar objetos que têm memória vazada.
    
Quando o método de logoff retorna, o MAPI chama o seguinte:
  
- O método **IUnknown:: Release** do objeto de logon. 
    
- O método **Shutdown** do objeto Provider para executar qualquer tarefa de limpeza final. Dependendo do tipo de provedor, um dos seguintes métodos é chamado: 
    
  - [IABProvider:: desligar](iabprovider-shutdown.md) para provedores de catálogo de endereços 
    
  - [IMSProvider:: desligar](imsprovider-shutdown.md) para provedores de repositórios de mensagens 
    
  - [IXPProvider:: desligar](ixpprovider-shutdown.md) para provedores de transporte 
    
- O método **IUnknown:: Release** do objeto Provider. 
    
Se seu provedor for um repositório de mensagens, uma chamada de cliente para [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) também iniciará o processo de desligamento. O **StoreLogoff** desliga um determinado provedor de armazenamento de mensagens e não tem efeito sobre a sessão. Apenas um provedor de repositório de mensagens pode ser desligado com esse método; Não há uma maneira explícita de desligar um determinado catálogo de endereços ou provedor de transporte. Para obter informações sobre como responder a uma chamada **StoreLogoff** , conFira desligamento [de um provedor de armazenamento de mensagens](shutting-down-a-message-store-provider.md).
  
A DLL do provedor será descarregada quando MAPI chamar a função de API Win32 **FreeLibrary**, uma chamada feita após o último cliente ativo chamou [MAPIUninitialize](mapiuninitialize.md). Nesse momento, o seu provedor de serviços terminará de ser desligado. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviço MAPI](mapi-service-providers.md)

