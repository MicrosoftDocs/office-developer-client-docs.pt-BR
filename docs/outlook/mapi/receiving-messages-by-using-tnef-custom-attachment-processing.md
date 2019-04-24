---
title: Recebendo mensagens usando o processamento de anexos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328424"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>Recebendo mensagens usando o processamento de anexos personalizado TNEF

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para receber uma mensagem TNEF com processamento de anexos personalizado:
  
1. Importe todas as propriedades de transmittable, que são compatíveis com o sistema de mensagens, da mensagem de entrada para uma nova mensagem MAPI. Isso inclui o texto da mensagem, que contém o fluxo de dados TNEF.
    
2. Identificar e decodificar o anexo especial que contém o fluxo TNEF.
    
3. Extraia todos os anexos da mensagem de entrada em anexos MAPI na nova mensagem MAPI. Os nomes de filerecuperáveis ou outros marcadores de identificação nos anexos devem ser colocados na propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) dos novos anexos para que o método [ITnef:: ExtractProps](itnef-extractprops.md) o pode posteriormente associar o anexo correto às marcas de anexo codificadas no texto da mensagem. 
    
4. Crie uma interface de **IStream** de OLE e entre em torno do fluxo TNEF decodificado e use esse objeto junto com a nova mensagem MAPI em uma chamada para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Chame o método **ITnef:: ExtractProps** para recuperar as propriedades nontransmittable na mensagem do fluxo de dados TNEF. 
    
6. Chame o método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) com os sinalizadores MAPI_CREATE e MAPI_MODIFY definidos. Essa chamada remove as marcas de anexo do texto da mensagem e as converte em informações de posição do anexo na mensagem MAPI. 
    
7. Entregar a mensagem pelo spooler MAPI.
    

