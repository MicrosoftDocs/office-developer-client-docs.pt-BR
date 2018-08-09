---
title: Liberar o provedor de transporte
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: b8032b22c78ae34bce7e9ccfb0f0a14cdde07290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770231"
---
# <a name="releasing-the-transport-provider"></a>Liberar o provedor de transporte

 
  
**Aplica-se a**: Outlook 
  
Quando MAPI ou o MAPI spooler termina usando um objeto de logon de transporte:
  
1. MAPI ou o MAPI spooler chama o método de [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) do provedor de transporte. 
    
2. O provedor de transporte invalida o objeto de status chamando o método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) . Se o provedor de transporte invalida objetos de mensagem que estão sendo enviadas ou recebidas no momento da chamada **TransportLogoff** dependem os sinalizadores que foram passados ao **TransportLogoff**.
    
3. O provedor de transporte chama o suporte ao método do objeto [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para remover a linha do provedor de transporte da tabela de status e remova qualquer identificadores exclusivos (UIDs) que foram definidos com o [IMAPISupport tabelas internas:: SetProviderUID](imapisupport-setprovideruid.md) método. Ele diminui a contagem de objetos de logon conhecidos ativos neste objeto provedor. Se a contagem chegar a zero, o MAPI chama o método [IXPProvider::Shutdown](ixpprovider-shutdown.md) e a **versão** no objeto provedor. Se este foi o último objeto fornecedor conhecido usando essa DLL sobre esse processo, MAPI chama a função de **FreeLibrary** na DLL mais tarde. Memória para o objeto de suporte MAPI seja liberada e retorna o objeto de suporte ao método de **lançamento** . 
    
4. O método **TransportLogoff** Retorna S_OK. 
    
5. MAPI ou o MAPI spooler chama a **versão** no objeto de logon do provedor de transporte. A memória para o objeto é liberada. 
    
6. MAPI ou o MAPI spooler chama **FreeLibrary** no provedor DLL. 
    
Para robustez, os objetos de logon e o provedor devem ser capazes de lidar com chamadas de **versão** finais em si mesma sem ter que primeiro suas **TransportLogoff** ou os métodos de **desligamento** chamados. Se a **versão** é chamado nesses casos, provedores de transporte devem tratar as chamadas como se **TransportLogoff** ou **desligamento** tivesse sido chamado com um argumento zero seguido de **lançamento**.
  

