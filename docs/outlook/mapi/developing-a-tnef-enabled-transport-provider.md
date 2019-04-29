---
title: Desenvolver um provedor de transporte habilitado para TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 282b1866699b695c647caedd130ce5abc1bcbc2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438999"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Desenvolver um provedor de transporte habilitado para TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para promover a interoperabilidade entre sistemas de mensagens que oferecem suporte a diferentes conjuntos de recursos MAPI, o MAPI fornece o formato de encapsulamento de transporte neutro (TNEF) como uma maneira padrão de transferir dados. Este formato encapsula as propriedades MAPI que não têm suporte de um sistema de mensagens subjacente em um fluxo binário que pode ser transferido junto com a mensagem quando um provedor de transporte o envia. O provedor de transporte que recebe a mensagem pode então decodificar o fluxo binário para recuperar todas as propriedades da mensagem original e disponibilizá-las aos aplicativos cliente. O modelo operacional para TNEF é:
  
- Os clientes de mensagens enviam e recebem mensagens para um transporte TNEF como normal.
    
- O transporte separa as propriedades nas mensagens de saída em duas categorias: as que o sistema de mensagens subjacente suporta e as que não. Os valores das propriedades que são compatíveis com o sistema de mensagens subjacente são convertidos no formato necessário.
    
- O transporte usa os métodos MAPI TNEF para codificar qualquer propriedade sem suporte em um único fluxo de dados. O transporte então transforma esse fluxo de dados em um anexo especial na mensagem de saída, usando o modelo de anexo do sistema de mensagens subjacente, antes de enviar a mensagem.
    
- Um transporte habilitado para TNEF que recebe tal mensagem faz duas coisas. Primeiro, ele converte as propriedades da mensagem de entrada, as quais há suporte no sistema de mensagens subjacente, em propriedades MAPI. Em segundo lugar, se o anexo especial estiver presente, ele usará os métodos de MAPI TNEF para recuperar propriedades MAPI adicionais do anexo antes de entregar a mensagem a um aplicativo cliente.
    
O MAPI fornece uma implementação da interface **ITnef** para uso por provedores de transporte MAPI ao trabalhar com objetos TNEF. A função [OpenTnefStreamEx](opentnefstreamex.md) é usada para criar objetos TNEF e associá-los a uma mensagem. Os fluxos TNEF são criados na parte superior da interface do OLE **IStream** 
  
> [!NOTE]
> Você usa o **OpenTnefStreamEx** para criar objetos TNEF. A função antiga do **OpenTnefStream** ainda existe para compatibilidade com código-fonte antigo e não deve ser usada em nada novo. 
  
A interface **ITnef** fornece os seguintes métodos: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
O modelo de implementação MAPI TNEF oferece suporte a:
  
- Todas as propriedades MAPI sem afetar outras propriedades de mensagem. Para que as mensagens MAPI sobrevivam transporte por meio de um sistema de mensagens, todas as propriedades que não podem ser codificadas como propriedades do sistema de mensagens devem ser encapsuladas. Como quase nunca é conhecido no momento em que uma mensagem é enviada independentemente de um cliente compatível com MAPI receber a mensagem, o esquema de encapsulamento permite que um provedor de transporte codifique apenas as propriedades de mensagens de MAPI que o sistema de mensagens não suporte nativo. Isso significa que as mensagens que usam TNEF não são "opacos" para sistemas de mensagens que não são baseados em MAPI, como sistemas de mensagens UNIX baseados em SMTP. Esses sistemas recebem as propriedades que eles suportam de qualquer maneira típica para eles, e outras propriedades são recebidas como um fluxo de dados TNEF codificado. O provedor de transporte TNEF é responsável por diferenciar esses dois conjuntos de propriedades e enviar o conjunto suportado da maneira adequada para o sistema de mensagens. O TNEF não faz suposições com o nível de suporte fornecido por um sistema de mensagens. No enTanto, nos exemplos de uso do TNEF incluídos nesta seção, pressupõe-se que o sistema de mensagens oferece suporte a pelo menos um anexo único além da mensagem. Em alguns casos, o anexo só pode ser suportado por meio de um fluxo UUEncoded e transmitido como parte do texto da mensagem. Somente em circunstâncias muito raras, o sistema de mensagens terá pouco suporte para propriedades de mensagens que a codificação TNEF completa de todas as propriedades seja necessária.
    
- Um mecanismo para determinar se um fluxo TNEF em uma mensagem de entrada pertence à mensagem, com base na propriedade MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Essa propriedade deve ser encontrada tanto no fluxo TNEF quanto em um cabeçalho de mensagem apropriado. Se a propriedade tiver o mesmo valor em ambos os locais ou se estiver ausente em qualquer lugar, presume-se que o fluxo de TNEF pertença à mensagem. Caso contrário, o fluxo TNEF será ignorado. Os transportes habilitados para TNEF são responsáveis por escolher um valor para essa propriedade em mensagens de saída e codificá-lo em um cabeçalho de mensagem apropriado (por exemplo, o cabeçalho Message-ID: cabeçalho para mensagens SMTP) e no fluxo TNEF.
    

