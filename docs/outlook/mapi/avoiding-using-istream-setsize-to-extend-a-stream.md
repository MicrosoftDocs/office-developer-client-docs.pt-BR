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
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766241"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Evitar o uso de IStream::SetSize para estender um fluxo

  
  
**Aplica-se a**: Outlook 
  
Ao gravar fluxos, em alguns casos, é necessário ampliá-las porque seu tamanho inicial não é mais suficiente. Use o método OLE **IStream::Write** para realizar essa tarefa, em vez de **IStream::SetSize**. **IStream::Write** automaticamente estende o fluxo, tornando * * IStream::SetSize * * desnecessárias. Chamar **IStream::Write** sem **IStream::SetSize** pode ser até três vezes mais rapidamente do que fazendo com que o **SetSize** chamada antes de **gravar**.
  

