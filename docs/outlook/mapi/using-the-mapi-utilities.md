---
title: Usar os utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3f461d50e838aac0caee37d295ba8e86b9559bd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770699"
---
# <a name="using-the-mapi-utilities"></a>Usar os utilitários MAPI

  
  
**Aplica-se a**: Outlook 
  
Os utilitários MAPI são compostos de dados da tabela e objetos de dados de propriedade e uma variedade de funções para dar suporte a diversos recursos. É possível para um cliente precisam apenas esses utilitários e não precisa fazer logon no subsistema de MAPI para estabelecer uma conexão com provedores de serviço. Se seu cliente enquadra nessa categoria, chamar a função de API [ScInitMapiUtil](scinitmapiutil.md) , e não a função [MAPIInitialize](mapiinitialize.md) em tempo de inicialização. 
  
 **ScInitMapiUtil** permite aos clientes utilizarem funções do utilitário que exigem alocadores de MAPI, mas que não solicitará as alocadores explicitamente. Quando for tempo para serem desligados, chame [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos ao invés [MAPIUninitialize](mapiuninitialize.md). Clientes que nunca chamada **MAPIInitialize** não devem chamar **MAPIUninitialize**.
  
Se você tiver telefonado **ScInitMapiUtil** em vez de **MAPIInitialize** e estiver usando tabelas por meio dos métodos **ITableData** , em vez de por meio dos métodos **IMAPITable** , lembre-se de que as notificações de tabela não funcionará. Notificações exigem o uso de bibliotecas de MAPI e [IMAPITable: IUnknown](imapitableiunknown.md).
  

