---
title: Propriedades de cadeia de caracteres MAPI
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
# <a name="mapi-string-properties"></a>Propriedades de cadeia de caracteres MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI provides three different property types to describe string properties:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Propriedades de cadeia de caracteres são mais comumente definidas como PT_TSTRING. O PT_TSTRING tipo de propriedade é compilado condicionalmente para um dos outros tipos de propriedade de cadeia de caracteres, dependendo se a macro UNICODE foi definida. PT_STRING8 descreve cadeias de caracteres terminadas por caractere nulo de 8 bits no formato ANSI; PT_UNICODE descreve cadeias de caracteres terminadas por byte nulo. 
  
Um cliente ou um provedor de serviços, ou o cliente e o provedor podem optar por dar suporte a cadeias de caracteres Unicode. Não é necessário. Um cliente que dá suporte apenas PT_STRING8 cadeias de caracteres pode operar com um provedor que oferece suporte a Unicode e vice-versa. Para habilitar essa interoperabilidade, os clientes e provedores de serviços passam um sinalizador, o sinalizador MAPI_UNICODE, para indicar que Unicode é suportado em métodos que envolvem a troca de cadeias de caracteres. 
  
Por exemplo, suponha que um cliente suporte Unicode e precise recuperar o nome de exibição de uma pasta. Todas as propriedades de PT_TSTRING cliente são compiladas para digitar PT_UNICODE. Quando o cliente chama o método [IMAPIProp::GetProps](imapiprop-getprops.md) da pasta **para** recuperar sua propriedade PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ele passa o sinalizador MAPI_UNICODE para solicitar que a cadeia de caracteres de nome de exibição seja retornada no formato Unicode. 
  
Os clientes e provedores de serviços precisam estar cientes de que especificar um conjunto de caracteres em uma chamada de método é apenas uma solicitação. O suporte a um ou a ambos os conjuntos de caracteres é de acordo com o implementador do objeto. No entanto, os provedores de serviços são incentivados a dar suporte a ambos os conjuntos de caracteres porque permite que eles alcancem uma distribuição mais difundida do que os provedores que suportam apenas um conjunto. 
  
As propriedades de cadeia de caracteres podem crescer para serem muito grandes, assim como propriedades binárias — propriedades que usam o tipo de propriedade PT_BINARY. Para facilitar o trabalho com propriedades grandes, o MAPI permite aos provedores de serviços definir essas propriedades para impor limites de tamanho. Esses limites podem variar, dependendo de:
  
- Se as propriedades estão sendo lidas ou escritas.
    
- Como o provedor de serviços implementa os **métodos IMAPIProp.** 
    
- Considerações sobre tempo de execução, como restrições de memória.
    
- Problemas de tradução do conjunto de caracteres. 
    
Os limites de tamanho também podem ser colocados em propriedades binárias e de cadeia de caracteres quando são usados no conjunto de colunas de uma tabela porque às vezes é impossível tornar visível todo o valor de uma propriedade grande. Muitos provedores de serviços truncam uma cadeia de caracteres grande ou propriedades binárias que são usadas em tabelas para 255 bytes. 
  
Quando um cliente chama o método **GetProps** ou **SetProps** de um objeto para trabalhar com uma propriedade binária ou cadeia de caracteres grande e a chamada falha devido ao tamanho da propriedade, o método retorna o valor de erro MAPI_E_NOT_ENOUGH_MEMORY. Se for **GetProps** que está falhando em uma propriedade específica, o cliente poderá recuperar chamando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e solicitando o **IStream** para acesso especificando IID_IStream como o identificador da interface. Usando **OpenProperty**, o cliente pode recuperar uma propriedade grande usando uma interface como **IStream** que é mais adequada para trabalhar com propriedades grandes. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

