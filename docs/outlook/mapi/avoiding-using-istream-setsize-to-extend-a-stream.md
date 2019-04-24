---
title: Evitando o uso do IStreamSetSize para estender um fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331619"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Evitando o uso de IStream:: SetSize para estender um fluxo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao gravar em fluxos, às vezes é necessário aumentá-los, pois seu tamanho inicial não é mais suficiente. Use o método OLE **IStream:: Write** para realizar isso em vez de **IStream:: SetSize**. **IStream:: Write** estende automaticamente o fluxo, fazendo * * IStream:: SetSize * * desnecessário. Chamar **IStream:: Write** sem **IStream:: SetSize** pode ser até três vezes mais rápido do que **** fazer a chamada SetSize antes da **gravação**.
  

