---
title: Iniciar sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9e95423a1aa9a04247a70592a797d2395cafecc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595367"
---
# <a name="starting-a-mapi-session"></a>Iniciar sessão MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Embora não haja uma quantidade significativa de trabalho executado durante a sessão de inicialização, as tarefas necessárias são mínimas. Muito desse trabalho é feito de MAPI processamento das chamadas [MAPIInitialize](mapiinitialize.md) e [MAPILogonEx](mapilogonex.md) . Ambas as funções aceitam sinalizadores como parâmetros de entrada para controlar os aspectos da sessão como tratamento de notificação e a interface do usuário. É importante entender as consequências de configuração de cada um desses sinalizadores ao chamar **MAPIInitialize** para inicializar as bibliotecas MAPI e **MAPILogonEx** para fazer logon no subsistema de MAPI. 
  
 **Para iniciar uma sessão MAPI**
  
1. Chame **MAPIInitialize** para inicializar o conjunto padrão de bibliotecas MAPI. 
    
2. Se você precisa usar as bibliotecas OLE, chamar a função OLE [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Se você precisar usar a biblioteca do utilitário MAPI, chame [ScInitMapiUtil](scinitmapiutil.md).
    
4. Chame **MAPILogonEx** com um perfil válido para fazer logon no subsistema de MAPI. **MAPILogonEx** verifica a configuração de cada um dos provedores de serviço nos serviços de mensagem incluídos no perfil, avisar o usuário para obter informações adicionais, se necessário e possíveis. Quando terminar de **MAPILogonEx** , os provedores de serviço configurado estão prontos para o serviço. 
    
## <a name="in-this-section"></a>Nesta seção

[Iniciar MAPI](initializing-mapi.md)
  
> Descreve como inicializar MAPI para uma sessão.
    
[Iniciar OLE para MAPI](initializing-ole-for-mapi.md)
  
> Descreve as chamadas para fazer para inicializar o OLE para uso com MAPI.
    
[Iniciar utilitários MAPI](initializing-the-mapi-utilities.md)
  
> Descreve como inicializar utilitários MAPI.
    
[Fazer logon no MAPI](logging-on-to-mapi.md)
  
> Descreve como aplicativos cliente faça logon no sistema de sub MAPI.
    

