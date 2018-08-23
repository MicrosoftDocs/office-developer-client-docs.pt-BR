---
title: Evitar o uso de IStreamSetSize para estender um fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9245d4913c2832b8c942093e65cf088643a1947c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592077"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Evitar usar IStream::SetSize para estender um fluxo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao gravar fluxos, em alguns casos, é necessário ampliá-las porque seu tamanho inicial não é mais suficiente. Use o método OLE **IStream::Write** para realizar essa tarefa, em vez de **IStream::SetSize**. **IStream::Write** automaticamente estende o fluxo, tornando * * IStream::SetSize * * desnecessárias. Chamar **IStream::Write** sem **IStream::SetSize** pode ser até três vezes mais rapidamente do que fazendo com que o **SetSize** chamada antes de **gravar**.
  

