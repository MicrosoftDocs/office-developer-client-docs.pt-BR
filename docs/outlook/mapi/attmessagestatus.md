---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430312"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Sinalizadores de mensagem MAPI são mapeados para sinalizadores TNEF para preservar a compatibilidade com compatibilidade. Todos os sinalizadores são agrupados e codificados em um único byte. Os mapeamentos são os seguinte:
  
|**Sinalizadores de mensagem MAPI**|**Sinalizadores TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Esses sinalizadores são definidos no TNEF. Arquivo de header H.
  

