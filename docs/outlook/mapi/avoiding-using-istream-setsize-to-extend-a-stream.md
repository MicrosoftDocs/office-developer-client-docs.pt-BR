---
title: Evitando o uso de IStreamSetSize para estender um fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428911"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Evitando o uso de IStream::SetSize para estender um fluxo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao escrever em fluxos, às vezes é necessário ampliá-los porque seu tamanho inicial não é mais suficiente. Use o método OLE **IStream::Write** para fazer isso em vez de **IStream::SetSize**. **IStream::Write** estende automaticamente o fluxo, tornando ** IStream::SetSize ** desnecessário. Chamar **IStream::Write** sem **IStream::SetSize** pode ser até três vezes mais rápido do que fazer a chamada **SetSize** antes de **Gravar.**
  

