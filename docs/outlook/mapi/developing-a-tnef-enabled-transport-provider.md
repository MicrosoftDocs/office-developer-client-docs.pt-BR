---
title: Desenvolver um provedor de transporte habilitado por TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7525eee1-4016-49b8-9509-5ebbe1db819f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4d4f7ed75bb1144b7cd4a813b0d093246a30cca5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588346"
---
# <a name="developing-a-tnef-enabled-transport-provider"></a>Desenvolver um provedor de transporte habilitado por TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para promover a interoperabilidade entre sistemas de mensagens que oferecem suporte a diferentes conjuntos de recursos MAPI, MAPI fornece o TNEF Transport Neutral Encapsulation Format () como uma maneira padrão para transferir dados. Esse formato encapsula propriedades MAPI não suportadas por um sistema de mensagens subjacente em um fluxo binário que pode ser transferido junto com a mensagem um provedor de transporte enviá-la. O provedor de transporte que recebe a mensagem, em seguida, pode decodificar o fluxo binário para recuperar todas as propriedades da mensagem original e torná-los disponíveis para os aplicativos cliente. O modelo operacional para TNEF é:
  
- Clientes de mensagens enviem e recebem mensagens para um transporte TNEF como de costume.
    
- O transporte separa as propriedades nas mensagens de saída em duas categorias: aqueles que suporta o sistema de mensagem subjacente e aqueles que não existir. Os valores das propriedades que são suportados pelo sistema de mensagens subjacente são convertidos em formato exigido.
    
- O transporte usa os métodos de MAPI TNEF codificar todas as propriedades sem suporte em um único fluxo de dados. O transporte, em seguida, transforma esse fluxo de dados em um anexo especial na mensagem de saída, usando o modelo de anexo do sistema de mensagens subjacentes, antes de enviar a mensagem.
    
- Um transporte TNEF habilitado que recebe uma mensagem tal faz duas coisas. Primeiro, ele converte propriedades da mensagem de entrada — aqueles compatíveis com o sistema de mensagem subjacente — para propriedades MAPI. Segundo, se o anexo especial estiver presente, ele usa os métodos de MAPI TNEF para recuperar as propriedades adicionais de MAPI do anexo antes de entregar a mensagem para um aplicativo cliente.
    
MAPI fornece uma implementação da interface **ITnef** para uso por provedores de transporte MAPI ao trabalhar com objetos TNEF. A função [OpenTnefStreamEx](opentnefstreamex.md) é usada para criar objetos TNEF e associá-los a uma mensagem. Fluxos TNEF baseiam-se na parte superior a interface **IStream** do OLE 
  
> [!NOTE]
> Você pode usar **OpenTnefStreamEx** para criar objetos TNEF. A função de **OpenTnefStream** antiga ainda existe apenas para compatibilidade com o antigo código-fonte e não deve ser usada em algo novo. 
  
A interface **ITnef** fornece os seguintes métodos: 
  
- [AddProps](itnef-addprops.md)
    
- [EncodeRecips](itnef-encoderecips.md)
    
- [ExtractProps](itnef-extractprops.md)
    
- [Finish](itnef-finish.md)
    
- [FinishComponent](itnef-finishcomponent.md)
    
- [OpenTaggedBody](itnef-opentaggedbody.md)
    
- [SetProps](itnef-setprops.md)
    
O modelo de implementação de MAPI TNEF suporta:
  
- Todas as propriedades MAPI sem afetar outras propriedades de mensagem. Em ordem para mensagens MAPI de sobrevivência transporte por meio de um sistema de mensagens, todas as propriedades que não podem ser codificadas como propriedades do sistema de mensagens devem ser encapsuladas. Porque quase nunca é conhecido no momento em que uma mensagem é enviada se ou não um cliente compatível com MAPI irá receber a mensagem, o esquema de encapsulamento permite que um provedor de transporte codificar apenas as propriedades de mensagem MAPI que o sistema de mensagens não suporte nativo. Isso significa que as mensagens que usam o TNEF não são "opacas" aos sistemas de mensagens que não são baseados em MAPI, como UNIX baseados em SMTP sistemas de mensagens. Esses sistemas recebem as propriedades que eles suportam na forma que é comum para-las e outras propriedades são recebidas como um fluxo de dados TNEF codificado. O provedor de transporte TNEF é responsável por distinguir entre esses dois conjuntos de propriedades e enviando o conjunto com suporte de maneira adequada para o sistema de mensagens. TNEF não faz nenhuma suposições como para o nível de suporte fornecido por um sistema de mensagens. No entanto, nos exemplos de uso TNEF incluído nesta seção, a pressuposição é feita que o sistema de mensagens oferece suporte a pelo menos um único anexo além da mensagem. Em alguns casos, o anexo só pode ser transmitido como parte do texto da mensagem e suportado por meio de um stream uuencoded. Somente em circunstâncias muito raras sistema de mensagens terão portanto pouco suporte para as propriedades de mensagem que codificação TNEF completo de todas as propriedades é necessário.
    
- Um mecanismo para determinar se um fluxo TNEF em uma mensagem de entrada pertence à mensagem, com base na propriedade de MAPI **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Esta propriedade deve estar presente no stream TNEF e em um cabeçalho de mensagem apropriada. Se a propriedade tem o mesmo valor em ambos os lugares, ou está falta em qualquer lugar, o fluxo TNEF é considerado pertencem à mensagem. Caso contrário, o fluxo TNEF será ignorado. Transportes TNEF habilitado são responsáveis por escolhendo um valor para essa propriedade em mensagens de saída e a codificação em um cabeçalho de mensagem apropriada (por exemplo, o Message-ID: cabeçalho para mensagens SMTP) e no stream TNEF.
    

