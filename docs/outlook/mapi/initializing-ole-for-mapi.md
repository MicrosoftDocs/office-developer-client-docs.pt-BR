---
title: Iniciar OLE para MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cd279c17574ce73b42d5e07e96ac817af71dc700
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589802"
---
# <a name="initializing-ole-for-mapi"></a>Iniciar OLE para MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se você usar também o OLE, chame a função OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) para inicializar as bibliotecas OLE. **OleInitialize** inicializa dados globais para a sessão e prepara as bibliotecas OLE aceite as chamadas. Para obter informações sobre a chamada **OleInitialize**, consulte o SDK do Windows.
  

