---
title: Inicializando os utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420945"
---
# <a name="initializing-the-mapi-utilities"></a>Inicializando os utilitários MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se a única parte de MAPI que você precisa usar são os utilitários as interfaces e funções declaradas no MAPIUTIL de MAPI. Arquivo de header H como **IPropData** e **ITableData** — você não precisa chamar **MAPIInitialize** para inicialização. Para obter mais informações, consulte [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)e [MAPIInitialize](mapiinitialize.md). Em vez disso, chame **a função ScInitMapiUtil.** Para obter mais informações, [consulte ScInitMapiUtil](scinitmapiutil.md). **O ScInitMapiUtil** permite que aplicativos cliente usem funções e métodos utilitários que exigem alocadores MAPI, mas que não os solicitam explicitamente. 
  
No momento do desligamento, faça uma chamada para **DeinitMapiUtil** para liberar recursos conectados aos utilitários. Não chame **MAPIUninitialize**. Para obter mais informações, [consulte DeinitMapiUtil](deinitmapiutil.md) e [MAPIUninitialize](mapiuninitialize.md).
  
Esteja ciente de que a interface **ITableData** não dá suporte a notificações de tabela para clientes que tenham chamado **ScInitMapiUtil** em vez de **MAPIInitialize**. 
  

