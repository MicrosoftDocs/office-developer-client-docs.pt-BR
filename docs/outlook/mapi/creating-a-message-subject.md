---
title: Criar um assunto de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cae255b90e8f2ccaaec4736c7ba1e9d6b7764f58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593106"
---
# <a name="creating-a-message-subject"></a>Criar um assunto de mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O assunto de uma mensagem, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), é uma propriedade opcional, usada para resumir a intenção de uma mensagem. Se você optar por defini-la, tornam uma cadeia de caracteres 128 bytes ou menos. O limite de 128 bytes não é um limite imposto pelo MAPI; é um limite imposto por alguns provedores de repositório de mensagem. Para assegurar a interoperabilidade com provedores que impõem-lo, limite assuntos a 128 bytes. 
  
Lembre-se de que alguns provedores de armazenamento de mensagem não permita **PR_SUBJECT** a serem gravados em um stream com a interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
  
Não definir **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Essa propriedade é definida somente em respostas e mensagens encaminhada. 
  

