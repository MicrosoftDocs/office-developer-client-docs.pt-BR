---
title: Propriedades da cadeia de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431390"
---
# <a name="mapi-string-properties"></a>Propriedades da cadeia de caracteres MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI fornece três tipos de propriedades diferentes para descrever Propriedades de cadeia de caracteres:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
As propriedades de cadeia de caracteres são mais comumente definidas como PT_TSTRING. O tipo de propriedade PT_TSTRING, condicionalmente, compila-se para um dos outros tipos de propriedade de cadeia de caracteres, dependendo de a macro UNICODE ter sido definida. PT_STRING8 descreve as cadeias de caracteres de 8 bits terminadas por nulo no formato ANSI; PT_UNICODE descreve as cadeias de caracteres de caractere nulo de byte duplo terminadas. 
  
Um cliente ou um provedor de serviços ou o cliente e o provedor podem optar por oferecer suporte a cadeias de caracteres Unicode. Não é necessário. Um cliente que oferece suporte somente a cadeias de caracteres do PT_STRING8 pode operar com um provedor que oferece suporte a Unicode e vice-versa. Para habilitar essa interoperabilidade, os clientes e provedores de serviço passam um sinalizador, o sinalizador MAPI_UNICODE, para indicar que há suporte para Unicode em métodos que envolvem a troca de cadeias de caracteres. 
  
Por exemplo, suponha que um cliente dê suporte a Unicode e precise recuperar o nome de exibição de uma pasta. Todas as propriedades de PT_TSTRING do cliente são compiladas para o tipo PT_UNICODE. Quando o cliente chama o método [IMAPIProp::](imapiprop-getprops.md) GetProps da pasta para recuperar sua propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ele passa o sinalizador MAPI_UNICODE para solicitar que a cadeia de caracteres do nome para exibição seja retornada no formato Unicode . 
  
Os clientes e provedores de serviços devem estar cientes de que a especificação de um conjunto de caracteres em uma chamada de método é apenas uma solicitação. O suporte a um ou a ambos os conjuntos de caracteres é até o implementador do objeto. No enTanto, os provedores de serviços são incentivados a oferecer suporte a ambos os conjuntos de caracteres, pois eles podem obter uma distribuição mais abrangente do que os provedores que dão suporte a apenas um conjunto. 
  
As propriedades de cadeia de caracteres podem aumentar para serem muito grandes como propriedades binárias, propriedades que usam o tipo de propriedade PT_BINARY. Para facilitar o trabalho com propriedades grandes, o MAPI permite que os provedores de serviços configurem essas propriedades para impor limites de tamanho. Esses limites podem variar, dependendo de:
  
- Se as propriedades estão sendo lidas ou gravadas.
    
- Como o provedor de serviços implementa os métodos **IMAPIProp** . 
    
- Considerações de tempo de execução, como restrições de memória.
    
- Problemas de conversão de conjunto de caracteres. 
    
Os limites de tamanho também podem ser colocados em Propriedades de cadeia de caracteres e binárias quando são usados no conjunto de colunas de uma tabela porque às vezes é impossível tornar todos os valores de propriedade grandes visíveis. Muitos provedores de serviços truncam Propriedades de cadeia de caracteres grandes ou binárias que são usadas em tabelas para 255 bytes. 
  
Quando um cliente chama o método getProps ou setProps de um objeto para trabalhar com uma cadeia de caracteres grande ou uma propriedade binária e a chamada falha devido ao tamanho da propriedade, o método retorna o valor de erro MAPI_E_NOT_ENOUGH_MEMORY. **** **** Se for getProps com falha para uma propriedade específica, o cliente poderá se recuperar chamando [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) e solicitando o **** **IStream** para acesso, especificando IID_IStream como o identificador de interface. Usando **OpenProperty**, o cliente pode recuperar uma propriedade grande usando uma interface como **IStream** que é mais adequada para trabalhar com propriedades grandes. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

