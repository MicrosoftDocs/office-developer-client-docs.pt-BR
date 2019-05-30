---
title: Propriedades canônicas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2fc605c57936765f43d7a6941dcc8d40d058db2f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540473"
---
# <a name="mapi-canonical-properties"></a>Propriedades canônicas MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma propriedade canônica é uma propriedade virtual que representa uma propriedade MAPI ou várias propriedades MAPI definidas com o mesmo identificador de propriedade. As propriedades canônicas destinam-se apenas a facilitar a identificação consistente de propriedades MAPI em discussões ou documentação fora do código. Diferentemente dos nomes de propriedade marcados de MAPI definidos, os nomes de propriedade canônica não são definidos como constantes globais em arquivos de cabeçalho MAPI.
  
## <a name="naming-conventions"></a>Convenções de nomenclatura

Os nomes de propriedades canônicas começam com um prefixo, "PID", que representa "identificador de propriedade". Dependendo se a propriedade é uma propriedade marcada, uma propriedade nomeada com um identificador numérico ou uma propriedade nomeada com um nome de cadeia de caracteres, o prefixo é mais qualificado como "PidTag", "PidLid" e "PidName", respectivamente. Por exemplo, [PidTagAccount](pidtagaccount-canonical-property.md) representa as propriedades marcadas, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) **, PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) e **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), que especificam o nome da conta; [PidLidContacts](pidlidcontacts-canonical-property.md) representa a propriedade **dispidContacts** , uma propriedade nomeada que tem um identificador numérico e que especifica o nome dos contatos associados a uma mensagem; e [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) representa "http://schemas.microsoft.com/outlook/phishingstamp," uma propriedade nomeada que tem um nome de cadeia de caracteres e que especifica a cadeia de caracteres marcando mensagens que provavelmente serão phishing. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Representando propriedades semelhantes usando uma propriedade canônica

### <a name="identifying-properties-in-mapi"></a>Identificando Propriedades no MAPI

Todas as propriedades no MAPI são identificadas por um identificador de propriedade que é um valor de 16 bits não assinado. O identificador de propriedade e o tipo de propriedade (outro valor de 16 bits não assinado) constituem uma marca de propriedade para a propriedade. 
  
MAPI usa uma marca de propriedade para definir exclusivamente Propriedades. As propriedades que têm a mesma marca de propriedade, como **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) e **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), são consideradas idênticas Propriedades em MAPI. Para obter uma lista de marcas de propriedade que o MAPI definiu para suas próprias propriedades, consulte o arquivo de cabeçalho MAPI, mapitags. h.
  
Observe que MAPI divide identificadores de propriedade em intervalos. Onde um identificador está no intervalo indica seu uso e propriedade. Os identificadores de propriedade das propriedades marcadas estão no intervalo de 0x0001 a 0x7FFF. Dentro desse intervalo, estão os identificadores de propriedade de propriedades definidas por MAPI, que estão no intervalo de 0x0001 a 0x3FFF. Os identificadores de propriedade das propriedades nomeadas estão no intervalo de 0x8000 a 0x8FFF. 
  
As propriedades nomeadas também são atribuídas por um conjunto de propriedades e uma ID longa (tampa), que é um valor de 32 bits não assinado ou uma cadeia de caracteres. Um conjunto de propriedades é um GUID que identifica um grupo de propriedades nomeadas com uma finalidade semelhante. O conjunto de propriedades e a tampa ou o nome da cadeia de caracteres são usados para obter ou definir a propriedade nomeada.
  
### <a name="property-type"></a>Tipo de propriedade

Além de identificadores, uma propriedade é atribuída por um tipo de dados que especifica o tipo de valor permitido para essa propriedade.
  
Para propriedades que são do tipo cadeia de caracteres, dependendo do suporte para Unicode na plataforma subjacente, a propriedade pode ser do tipo PT_STRING8 (cadeia de caracteres de 8 bits terminada em nulo) ou PT_UNICODE (cadeia de caracteres Unicode terminada em nulo). Uma propriedade pode ser definida com o tipo PT_TSTRING e dependendo das configurações de compilação, o PT_TSTRING padrão para uma cadeia de caracteres Unicode para plataformas que oferecem suporte a Unicode ou para uma cadeia de caracteres PT_STRING8 para plataformas que dão suporte a ANSI ou DBCS. É comum que uma propriedade de tipo de cadeia de caracteres seja identificada por três nomes semelhantes, como **PR_ACCOUNT**, **PR_ACCOUNT_A**e **PR_ACCOUNT_W**, que são do tipo PT_TSTRING, PT_STRING8 e PT_UNICODE, respectivamente.
  
Para obter mais informações sobre tipos de propriedade e macros relacionados a tipos, consulte o arquivo de cabeçalho MAPI, mapidefs. h.
  
### <a name="identifying-similar-properties"></a>Identificando propriedades semelhantes

Na propriedade MAPI atual Landscape, não é incomum encontrar uma propriedade que tenha sido exposta em diferentes nomes de propriedades, todos eles definidos com o mesmo identificador de propriedade. Por exemplo, as propriedades marcadas, **PR_BUSINESS2_TELEPHONE_NUMBER** e **PR_OFFICE2_TELEPHONE_NUMBER**, são definidas em mapitags. h para ter o mesmo tipo e identificador de propriedade. Intimamente relacionadas a essas duas propriedades são:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
As propriedades com o sufixo "_A" são digitadas como PT_STRING8, e aquelas com o sufixo "_W" são digitadas como PT_UNICODE.
  
O objetivo de uma propriedade canônica, **PidTagBusiness2TelephoneNumber** neste exemplo, é facilitar a referência de propriedades MAPI afiliadas de maneira mais rigorosa usando um identificador e, de forma consistente (usando o prefixo "PID") em todos os MAPI Propriedades. Para localizar quais propriedades MAPI reais representa uma propriedade canônica, confira [mapeamento de nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md). Para localizar a propriedade canônica à qual uma propriedade MAPI está associada, confira [mapeamento de nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>Suporte MAPI de nomes de propriedades canônicas

Como as propriedades canônicas não são propriedades reais e não estão definidas em arquivos de cabeçalho MAPI, você não deve usar nomes de propriedades canônicas no código; em vez disso, você deve continuar a usar os nomes de propriedade MAPI exatas no código. Por exemplo, você pode fazer referência a **PR_BUSINESS2_TELEPHONE_NUMBER** e **PR_OFFICE2_TELEPHONE_NUMBER** fora do código como **PidTagBusiness2TelephoneNumber**e usar **PR_BUSINESS2_TELEPHONE_NUMBER** ou **PR_OFFICE2_ TELEPHONE_NUMBER** no código. 
  
Se você precisar usar nomes de propriedades canônicas no seu código, primeiro você deve defini-los em seus próprios arquivos de cabeçalho.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Nomes de propriedades canônicas e especificações do protocolo Exchange

Os nomes canônicos são referenciados nas especificações de protocolo do Microsoft Exchange Server usadas pelo Exchange Server para se comunicar com outros produtos da Microsoft. Para obter mais informações sobre as propriedades do objeto Message referenciadas pelas especificações do protocolo Exchange, consulte [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Confira também



[Marcas de propriedade MAPI](mapi-property-tags.md)
  
[Visão geral do identificador de propriedade MAPI](mapi-property-identifier-overview.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)

