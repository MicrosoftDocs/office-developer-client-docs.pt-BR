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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409983"
---
# <a name="using-the-mapi-utilities"></a>Usando os utilitários MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os utilitários MAPI são feitos de dados de tabela e objetos de dados de propriedade e uma variedade de funções para dar suporte a recursos diversos. É possível que um cliente precise apenas desses utilitários e não precise fazer logoff no subsistema MAPI para estabelecer uma conexão com provedores de serviços. Se seu cliente se encaixar nessa categoria, chame a função API [ScInitMapiUtil](scinitmapiutil.md) em vez da função [MAPIInitialize](mapiinitialize.md) no momento da inicialização. 
  
 **ScInitMapiUtil** permite que os clientes usem funções de utilitário que exigem alocadores MAPI, mas que não solicitam os alocadores explicitamente. Quando for o momento de desligar, chame [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos em vez de [MAPIUninitialize](mapiuninitialize.md). Clientes que nunca chamam **MAPIInitialize** não devem chamar **MAPIUninitialize**.
  
Se você tiver chamado **ScInitMapiUtil** em vez de **MAPIInitialize** e estiver usando tabelas por meio dos métodos **ITableData** em vez dos métodos **IMAPITable,** esteja ciente de que as notificações de tabela não funcionarão. As notificações exigem o uso das bibliotecas MAPI e [IMAPITable : IUnknown](imapitableiunknown.md).
  

