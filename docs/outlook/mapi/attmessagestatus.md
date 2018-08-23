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
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565743"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Sinalizadores de mensagem MAPI são mapeadas para TNEF sinalizadores para preservar a compatibilidade com versões anteriores. Todos os sinalizadores são agrupados e codificados em um único byte. Os mapeamentos são:
  
|**Sinalizadores de mensagem MAPI**|**Sinalizadores TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Esses sinalizadores são definidos no TNEF. Arquivo de cabeçalho H.
  

