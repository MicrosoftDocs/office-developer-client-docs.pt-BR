---
title: Iniciando uma sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336341"
---
# <a name="starting-a-mapi-session"></a>Iniciando uma sessão MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Embora haja uma quantidade significativa de trabalho executada durante a início da sessão, as tarefas necessárias são mínimas. Grande parte desse trabalho é feita no processamento MAPI das chamadas [MAPIInitialize](mapiinitialize.md) e [MAPILogonEx.](mapilogonex.md) Ambas as funções aceitam sinalizadores como parâmetros de entrada para controlar aspectos da sessão, como o tratamento de notificações e a interface do usuário. É importante compreender as consequências da configuração de cada um desses sinalizadores ao chamar **MAPIInitialize** para inicializar as bibliotecas MAPI e **MAPILogonEx** para fazer logoff no subsistema MAPI. 
  
 **Para iniciar uma sessão MAPI**
  
1. Chame **MAPIInitialize para** inicializar o conjunto padrão de bibliotecas MAPI. 
    
2. Se você precisar usar as bibliotecas OLE, chame a função [OLE OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Se você precisar usar a biblioteca de utilitários MAPI, chame [ScInitMapiUtil](scinitmapiutil.md).
    
4. Chame **MAPILogonEx com** um perfil válido para fazer logoff no subsistema MAPI. **O MAPILogonEx** verifica a configuração de cada um dos provedores de serviço nos serviços de mensagem incluídos no perfil, solicitando ao usuário informações adicionais, se necessário e possível. Quando **o MAPILogonEx** é concluído, os provedores de serviços configurados estão prontos para o serviço. 
    
## <a name="in-this-section"></a>Nesta seção

[Iniciar MAPI](initializing-mapi.md)
  
> Descreve como inicializar o MAPI para uma sessão.
    
[Iniciar OLE para MAPI](initializing-ole-for-mapi.md)
  
> Descreve as chamadas a fazer para inicializar o OLE para uso com MAPI.
    
[Inicializando os utilitários MAPI](initializing-the-mapi-utilities.md)
  
> Descreve como inicializar utilitários MAPI.
    
[Fazer logon no MAPI](logging-on-to-mapi.md)
  
> Descreve como os aplicativos cliente se registram no subsistema MAPI.
    

