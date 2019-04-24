---
title: Usando os utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329628"
---
# <a name="using-the-mapi-utilities"></a>Usando os utilitários MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os utilitários MAPI são compostos de dados de tabela e objetos de dados de propriedade e uma variedade de funções para dar suporte a recursos diversos. É possível que um cliente precise apenas desses utilitários e não precise fazer logon no subsistema MAPI para estabelecer uma conexão com os provedores de serviço. Se o cliente couber nessa categoria, chame a função da API [ScInitMapiUtil](scinitmapiutil.md) em vez da função [MAPIInitialize](mapiinitialize.md) no momento da inicialização. 
  
 O **ScInitMapiUtil** permite que os clientes usem funções utilitárias que exigem alocadores MAPI, mas que não solicitam os alocadores explicitamente. Quando for o momento de desligar, chame [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos, em vez de [MAPIUninitialize](mapiuninitialize.md). Clientes que nunca chamam **MAPIInitialize** não devem chamar **MAPIUninitialize**.
  
Se você chamou **ScInitMapiUtil** em vez de **MAPIInitialize** e está usando tabelas por meio dos métodos **ITableData** , e não através dos métodos IMAPITable, lembre-se de que as notificações de tabela não funcionarão. **** As notificações exigem o uso das bibliotecas MAPI e [IMAPITable: IUnknown](imapitableiunknown.md).
  

