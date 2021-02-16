---
title: Desenvolvendo um provedor TNEF-Enabled transporte de conteúdo
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
# <a name="developing-a-tnef-enabled-transport-provider"></a>Desenvolvendo um provedor TNEF-Enabled transporte de conteúdo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para promover a interoperabilidade entre sistemas de mensagens que suportam diferentes conjuntos de recursos MAPI, o MAPI fornece o TNEF (Transport Neutral Encapsulation Format) como uma maneira padrão de transferir dados. Esse formato encapsula as propriedades MAPI não suportadas por um sistema de mensagens subjacente em um fluxo binário que pode ser transferido junto com a mensagem quando um provedor de transporte o envia. O provedor de transporte que recebe a mensagem pode decodificar o fluxo binário para recuperar todas as propriedades da mensagem original e torná-las disponíveis para aplicativos cliente. O modelo operacional para TNEF é:
  
- Os clientes de mensagens enviam e recebem mensagens para um transporte TNEF normalmente.
    
- O transporte separa as propriedades das mensagens de saída em duas categorias: as que o sistema de mensagens subjacente suporta e as que ele não suporta. Os valores das propriedades que são suportadas pelo sistema de mensagens subjacente são convertidos no formato necessário.
    
- O transporte usa os métodos TNEF MAPI para codificar as propriedades sem suporte em um único fluxo de dados. Em seguida, o transporte transforma esse fluxo de dados em um anexo especial na mensagem de saída, usando o modelo de anexo do sistema de mensagens subjacente, antes de enviar a mensagem.
    
- Um transporte habilitado para TNEF que recebe essa mensagem faz duas coisas. Primeiro, ele converte as propriedades da mensagem de entrada — aquelas suportadas pelo sistema de mensagens subjacentes — em propriedades MAPI. Segundo, se o anexo especial estiver presente, ele usará os métodos TNEF MAPI para recuperar propriedades MAPI adicionais do anexo antes de entregar a mensagem para um aplicativo cliente.
    
O MAPI fornece uma implementação da interface **ITnef** para uso por provedores de transporte MAPI ao trabalhar com objetos TNEF. A [função OpenTnefStreamEx](opentnefstreamex.md) é usada para criar objetos TNEF e associá-los a uma mensagem. Fluxos TNEF são construídos sobre a interface **IStream** OLE 
  
> [!NOTE]
> Use **OpenTnefStreamEx** para criar objetos TNEF. A função **OpenTnefStream** antiga ainda existe para compatibilidade com o código-fonte antigo e não deve ser usada em nada novo. 
  
A interface **ITnef** fornece os seguintes métodos: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
O modelo de implementação TNEF MAPI oferece suporte a:
  
- Todas as propriedades MAPI sem afetar outras propriedades da mensagem. Para que as mensagens MAPI sobreviverem ao transporte por meio de um sistema de mensagens, todas as propriedades que não podem ser codificadas como propriedades do sistema de mensagens devem ser encapsuladas. Como é quase nunca conhecido no momento em que uma mensagem é enviada se um cliente compatível com MAPI receberá ou não a mensagem, o esquema de encapsulamento permite que um provedor de transporte codificar apenas as propriedades de mensagem MAPI às que o sistema de mensagens não suporta na nações. Isso significa que as mensagens que usam TNEF não são "opacos" para sistemas de mensagens que não são baseados em MAPI, como sistemas de mensagens UNIX baseados em SMTP. Esses sistemas recebem as propriedades às quais suportam de qualquer maneira, e outras propriedades são recebidas como um fluxo de dados TNEF codificado. O provedor de transporte TNEF é responsável por diferenciar entre esses dois conjuntos de propriedades e enviar o conjunto com suporte da maneira adequada para o sistema de mensagens. O TNEF não faz suposições sobre o nível de suporte fornecido por um sistema de mensagens. No entanto, nos exemplos de uso de TNEF incluídos nesta seção, a suposição é feita de que o sistema de mensagens oferece suporte a pelo menos um único anexo além da mensagem. Em alguns casos, o anexo só pode ter suporte por meio de um fluxo uuencoded e transmitido como parte do texto da mensagem. Somente em circunstâncias muito raras o sistema de mensagens terá tão pouco suporte para propriedades de mensagem que a codificação TNEF completa de todas as propriedades é necessária.
    
- Um mecanismo para determinar se um fluxo TNEF em uma mensagem de entrada pertence à mensagem, com base na propriedade MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Essa propriedade deve ser encontrada no fluxo TNEF e em um header de mensagem apropriado. Se a propriedade tiver o mesmo valor em ambos os lugares ou estiver ausente em ambos os locais, o fluxo TNEF será assumido como pertencendo à mensagem. Caso contrário, o fluxo TNEF será ignorado. Os transporte habilitados para TNEF são responsáveis por escolher um valor para essa propriedade em mensagens de saída e codificar-a em um header de mensagem apropriado (por exemplo, o message-ID: header para mensagens SMTP) e no fluxo TNEF.
    

