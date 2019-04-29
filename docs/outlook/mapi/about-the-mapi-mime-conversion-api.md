---
title: Sobre a API de conversão MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420434"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Sobre a API de conversão MAPI-MIME

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API de conversão MAPI-MIME permite que os provedores de email convertam objetos MIME e mensagens MAPI. Ele fornece definições constantes, identificadores de classe e identificadores de interface, conforme mostrado nas [constantes MAPI](mapi-constants.md). Os provedores de email devem Cocriar uma instância do **[IConverterSession](iconvertersessioniunknown.md)** chamando a função **CoCreateInstance** . 
  

