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
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766213"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Aplica-se a**: Outlook 
  
Sinalizadores de mensagem MAPI são mapeadas para TNEF sinalizadores para preservar a compatibilidade com versões anteriores. Todos os sinalizadores são agrupados e codificados em um único byte. Os mapeamentos são:
  
|**Sinalizadores de mensagem MAPI**|**Sinalizadores TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Esses sinalizadores são definidos no TNEF. Arquivo de cabeçalho H.
  

