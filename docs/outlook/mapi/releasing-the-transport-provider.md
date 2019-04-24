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
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328382"
---
# <a name="releasing-the-transport-provider"></a>Liberar o provedor de transporte

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando o MAPI ou o spooler MAPI termina de usar um objeto de logon de transporte:
  
1. O MAPI ou o spooler MAPI chama o método [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) do provedor de transporte. 
    
2. O provedor de transporte invalida o objeto status chamando o método [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) . Se o provedor de transporte invalida os objetos de mensagem que estão sendo enviados ou recebidos no momento da chamada **TransportLogoff** depende dos sinalizadores que foram passados para o **TransportLogoff**.
    
3. O provedor de transporte chama o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do objeto support para remover a linha do provedor de transporte da tabela status e remover de tabelas internas qualquer identificador exclusivo (UIDs) que foram definidos com o [IMAPISupport:: Método SetProviderUID](imapisupport-setprovideruid.md) . Ele diminui a contagem de objetos de logon conhecidos ativos neste objeto provedor. Se a contagem chegar a zero, o MAPI chamará o método [IXPProvider:: Shutdown](ixpprovider-shutdown.md) e o **lançamento** no objeto Provider. Se esse for o último objeto provedor conhecido usando essa DLL nesse processo, MAPI chamará a função **FreeLibrary** na DLL mais tarde. A memória do objeto de suporte MAPI é liberada e o método de **lançamento** do objeto support retorna. 
    
4. O método **TransportLogoff** retorna S_OK. 
    
5. O MAPI ou o spooler MAPI chama o **lançamento** no objeto de logon do provedor de transporte. A memória do objeto é liberada. 
    
6. O MAPI ou o spooler MAPI chama **FreeLibrary** na DLL do provedor. 
    
Para robustez, o logon e os objetos do provedor devem ser capazes de lidar com as chamadas de **versão** final por conta própria, sem antes ter seus métodos **TransportLogoff** ou **Shutdown** chamados. Se a **versão** for chamada nesses casos, os provedores de transporte devem tratar as chamadas como se **TransportLogoff** ou **Shutdown** tivesse sido chamado com um argumento zero seguido por **Release**.
  

