---
title: Criar um assunto de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395683"
---
# <a name="creating-a-message-subject"></a>Criar um assunto de mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O assunto de uma mensagem, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), é uma propriedade opcional, usada para resumir a intenção de uma mensagem. Se você optar por defini-la, tornam uma cadeia de caracteres 128 bytes ou menos. O limite de 128 bytes não é um limite imposto pelo MAPI; é um limite imposto por alguns provedores de repositório de mensagem. Para assegurar a interoperabilidade com provedores que impõem-lo, limite assuntos a 128 bytes. 
  
Lembre-se de que alguns provedores de armazenamento de mensagem não permita **PR_SUBJECT** a serem gravados em um stream com a interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
  
Não definir **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Essa propriedade é definida somente em respostas e mensagens encaminhada. 
  

