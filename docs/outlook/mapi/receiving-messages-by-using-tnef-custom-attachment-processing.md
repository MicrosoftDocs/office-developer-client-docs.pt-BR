---
title: Receber mensagens usando o processamento de anexos personalizado com TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 18fc0983554284355dcdfb301fd41a0161a860fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770236"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Receber mensagens usando o processamento de anexos personalizado com TNEF

 
  
**Aplica-se a**: Outlook 
  
Para receber uma mensagem TNEF com processamento de anexo personalizada:
  
1. Importar todas as propriedades transmittable — aqueles que suporta o sistema de mensagens — da mensagem de entrada em uma nova mensagem MAPI. Isso inclui o texto da mensagem, que contém o fluxo de dados TNEF.
    
2. Identifique e decodificar o anexo especial que contém o fluxo TNEF.
    
3. Extraia todos os anexos da mensagem de entrada em anexos de MAPI sobre a nova mensagem MAPI. Os nomes de arquivo recuperado ou outro marcadores de identificação sobre os anexos, devem ser colocado na propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) os anexos de novo assim que o método [ITnef::ExtractProps](itnef-extractprops.md) mais tarde pode associar o anexo correto com as marcas de anexo codificadas no texto da mensagem. 
    
4. Crie uma interface **IStream** do OLE para quebrar em torno do fluxo TNEF decodificado e usar esse objeto, juntamente com a nova mensagem MAPI em uma chamada para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Chame o método **ITnef::ExtractProps** para recuperar as propriedades de nontransmittable na mensagem de fluxo de dados TNEF. 
    
6. Chame o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) com o conjunto de sinalizadores MAPI_CREATE e MAPI_MODIFY. Essa chamada remove as marcas de anexo do texto da mensagem e converte-os em informações de posição de anexo na mensagem de MAPI. 
    
7. Entrega a mensagem por meio do spooler MAPI.
    

