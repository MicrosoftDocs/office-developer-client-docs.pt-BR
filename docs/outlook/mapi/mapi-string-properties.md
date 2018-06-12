---
title: Propriedades de cadeia de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3cf118866bbc305678201a42a9a91998334f5cb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767959"
---
# <a name="mapi-string-properties"></a>Propriedades de cadeia de caracteres MAPI

  
  
**Aplica-se a**: Outlook 
  
MAPI fornece três tipos de propriedade diferentes para descrever as propriedades de cadeia de caracteres:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Propriedades de cadeia de caracteres mais comumente são definidas como PT_TSTRING. O tipo de propriedade PT_TSTRING condicionalmente é compilado em um dos outros string propriedade tipos, dependendo dependendo se a macro UNICODE tiver sido definida. PT_STRING8 descreve cadeias de caracteres terminada em nulo de 8 bits no formato ANSI; PT_UNICODE descreve as cadeias de caracteres do caractere de byte duplo terminada em nulo. 
  
Como um cliente ou um provedor de serviço, ou cliente e provedor podem optar por oferecer suporte a cadeias de caracteres Unicode. Não é necessário. Um cliente que suporta apenas PT_STRING8 cadeias de caracteres pode operar com um provedor que ofereça suporte a Unicode e vice-versa. Para habilitar essa interoperabilidade, clientes e provedores de serviços passam um sinalizador, o sinalizador MAPI_UNICODE, para indicar que há suporte para nos métodos que envolvem a troca de cadeias de caracteres Unicode. 
  
Por exemplo, suponha que um cliente dá suporte a Unicode e precisa recuperar o nome de exibição de uma pasta. Todas as propriedades PT_TSTRING do cliente são compiladas para digitar PT_UNICODE. Quando o cliente chama o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da pasta para recuperar sua propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), passa o sinalizador MAPI_UNICODE para solicitar que a cadeia de caracteres de nome de exibição retornado no formato Unicode . 
  
Clientes e provedores de serviços precisam estar ciente de que a especificação de um conjunto em uma chamada de método de caracteres é apenas uma solicitação. Suporte a um ou ambos os conjuntos de caracteres é até o implementador do objeto. No entanto, os provedores de serviços são incentivados a oferecer suporte a ambos os conjuntos de caracteres porque ela permite que eles tenham mais difundida distribuição que os provedores que oferecem suporte a apenas um conjunto. 
  
Propriedades de cadeia de caracteres podem crescer para ser muito grande, como podem propriedades binárias — digite de propriedades que usam a propriedade PT_BINARY. Para facilitar a trabalhar com propriedades de grandes, MAPI permite que os provedores de serviço configuração dessas propriedades para impor limites de tamanho. Esses limites podem variar, dependendo de:
  
- Se as propriedades estão sendo lidos ou gravados.
    
- Como o provedor de serviço implementa os métodos **IMAPIProp** . 
    
- Considerações de tempo de execução, como restrições de memória.
    
- Problemas de conversão de conjunto de caracteres. 
    
Limites de tamanho também podem ser colocados em cadeia de caracteres e conjunto de propriedades binárias quando eles são usados na coluna de uma tabela porque às vezes é impossível tornar todos um grande valor de propriedade visível. Muitos provedores de serviço truncam grande cadeia de caracteres ou propriedades binárias que são usadas nas tabelas a 255 bytes. 
  
Quando um cliente chama um método do objeto **GetProps** ou **SetProps** para trabalhar com uma grande cadeia de caracteres ou uma propriedade binária e a chamada falhar devido ao tamanho da propriedade, o método retornará o valor de erro MAPI_E_NOT_ENOUGH_MEMORY. Se for **GetProps** que está falhando para uma propriedade específica, o cliente pode recuperar chamando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e solicitando **IStream** para acesso especificando IID_IStream como o identificador de interface. Usando **OpenProperty**, o cliente pode recuperar uma propriedade grande usando uma interface como **IStream** que é mais adequada para trabalhar com propriedades de grande porte. 
  
## <a name="see-also"></a>Confira também



[Vis�o geral da propriedade MAPI](mapi-property-overview.md)

