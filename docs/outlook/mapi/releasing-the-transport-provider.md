---
title: Liberando o provedor de transporte
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
# <a name="releasing-the-transport-provider"></a>Liberando o provedor de transporte

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando o Spooler MAPI ou MAPI termina de usar um objeto de logon de transporte:
  
1. MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method. 
    
2. O provedor de transporte invalida o objeto de status chamando o [método IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md) Se o provedor de transporte invalida os objetos de mensagem que estão sendo enviados ou recebidos no momento da chamada **TransportLogoff** depende dos sinalizadores que foram passados para **TransportLogoff**.
    
3. O provedor de transporte chama o método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do objeto de suporte para remover a linha do provedor de transporte da tabela de status e remover das tabelas internas quaisquer identificadores exclusivos (UIDs) que foram definidos com o método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md) Ele diminui a contagem de objetos de logon conhecidos ativos neste objeto de provedor. Se a contagem atingir zero, o MAPI chamará o método [IXPProvider::Shutdown](ixpprovider-shutdown.md) e **Release** no objeto do provedor. Se esse for o último objeto de provedor conhecido que usa essa DLL nesse processo, o MAPI chamará a **função FreeLibrary** na DLL posteriormente. A memória para o objeto de suporte MAPI é liberada e o método **Release** do objeto de suporte retorna. 
    
4. O **método TransportLogoff** retorna S_OK. 
    
5. MAPI or the MAPI spooler **calls Release** on the transport provider's logon object. A memória do objeto é liberada. 
    
6. MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL. 
    
Para robustez, os objetos de logon e provedor devem ser capazes de lidar com chamadas finais **de** Versão por conta própria sem antes ter seus métodos **TransportLogoff** ou **Shutdown** chamados. Se **Release** for chamado nesses casos, os provedores de transporte deverão tratar as chamadas como se **TransportLogoff** ou **Shutdown** tivessem sido chamados com um argumento zero seguido de **Release**.
  

