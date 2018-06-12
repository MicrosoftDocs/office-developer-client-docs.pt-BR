---
title: Inicializando OLE para MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767549"
---
# <a name="initializing-ole-for-mapi"></a>Inicializando OLE para MAPI

  
  
**Aplica-se a**: Outlook 
  
Se você usar também o OLE, chame a função OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) para inicializar as bibliotecas OLE. **OleInitialize** inicializa dados globais para a sessão e prepara as bibliotecas OLE aceite as chamadas. Para obter informações sobre a chamada **OleInitialize**, consulte o SDK do Windows.
  

