---
title: Iniciar utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8ee0504d4a8b9e2ce96e42a53b778d4e3f518fcc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767556"
---
# <a name="initializing-the-mapi-utilities"></a>Iniciar utilitários MAPI

  
  
**Aplica-se a**: Outlook 
  
Se a única parte do MAPI que você precise usar são os utilitários — as funções e interfaces declaradas na MAPIUTIL do MAPI. Arquivo de cabeçalho H como **IPropData** e **ITableData** — não é necessário chamar **MAPIInitialize** para inicialização. Para obter mais informações, consulte [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)e [MAPIInitialize](mapiinitialize.md). Em vez disso, chame a função de **ScInitMapiUtil** . Para obter mais informações, consulte [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** permite que os aplicativos cliente usar funções de utilitário e métodos que exigem alocadores de MAPI, mas que não pergunte explicitamente para eles. 
  
No horário de desligamento, fazer uma chamada para **DeinitMapiUtil** para liberar recursos conectado aos utilitários. Não chame **MAPIUninitialize**. Para obter mais informações, consulte [DeinitMapiUtil](deinitmapiutil.md) e [MAPIUninitialize](mapiuninitialize.md).
  
Lembre-se de que a interface **ITableData** não suporta as notificações de tabela para clientes que têm chamado **ScInitMapiUtil** em vez de **MAPIInitialize**. 
  

