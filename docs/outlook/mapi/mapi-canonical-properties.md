---
title: Propriedades MAPI canônicas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4b017089a675727703de9e2ed4d584e7f77a778a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401563"
---
# <a name="mapi-canonical-properties"></a>Propriedades MAPI canônicas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma propriedade canônica é uma propriedade virtual que representa uma propriedade MAPI ou várias propriedades MAPI definidas com o mesmo identificador de propriedade. Propriedades canônicas destinam-se apenas para facilitar a identificação consistente das propriedades MAPI em discussões ou documentação fora do código. Ao contrário dos nomes de propriedade marcados definida pelo MAPI, nomes de propriedade canônico não estão definidos como constantes globais nos arquivos de cabeçalho MAPI.
  
## <a name="naming-conventions"></a>Convenções de nomeação

Nomes de propriedade canônico começam com um prefixo, "Pid", que representa o "identificador de propriedade." Dependendo se a propriedade é uma propriedade marcada, uma propriedade nomeada com um identificador numérico ou uma propriedade nomeada com um nome de cadeia de caracteres, o prefixo é ainda mais qualificado como "PidTag", "PidLid" e "PidName" respectivamente. Por exemplo, [PidTagAccount](pidtagaccount-canonical-property.md) representa as propriedades marcadas, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) e **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), que especificam um destinatário nome da conta; [PidLidContacts](pidlidcontacts-canonical-property.md) representa a propriedade **dispidContacts** , uma propriedade nomeada que tenha um identificador numérico e que especifica o nome do contatos associados a uma mensagem. e [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) representa "https://schemas.microsoft.com/outlook/phishingstamp," uma propriedade nomeada que tem um nome de cadeia de caracteres, e que especifica a cadeia de caracteres marcando as mensagens que são provavelmente phishing. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Que representam propriedades semelhantes usando uma propriedade canônica

### <a name="identifying-properties-in-mapi"></a>Identificar propriedades MAPI

Todas as propriedades na MAPI são identificadas por um identificador de propriedade que é um valor de 16 bits não assinado. O identificador de propriedade e o tipo de propriedade (outro valor de 16 bits não assinado) constituem uma marca de propriedade para a propriedade. 
  
MAPI usa uma marca de propriedade para definir propriedades de exclusivamente. Propriedades que têm a mesma propriedade marca, como **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) e **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), são consideradas idênticas Propriedades no MAPI. Para obter uma lista das marcas de propriedade MAPI tenha definido para suas próprias propriedades, consulte o arquivo de cabeçalho MAPI, Mapitags.h.
  
Observe que o MAPI divide identificadores de propriedade em intervalos. Onde um identificador cai no intervalo indica seu uso e a propriedade. Os identificadores de propriedade das propriedades marcados se encaixam no intervalo de 0x0001 para 0x7FFF. Dentro desse intervalo são os identificadores de propriedade das propriedades definidas pelo MAPI, que se encaixam no intervalo de 0x0001 para 0x3FFF. Os identificadores de propriedade de queda de propriedades nomeadas no intervalo de 0x8000 para 0x8FFF. 
  
Além disso, propriedades nomeadas são atribuídas por um conjunto de propriedades e um longo ID (tampa), que é um valor de 32 bits não assinado, ou um string. Um conjunto de propriedades é um GUID que identifica um grupo de propriedades nomeadas com uma finalidade similar. O conjunto de propriedades e o nome LID ou cadeia de caracteres são usados para obter ou definir a propriedade nomeada.
  
### <a name="property-type"></a>Tipo de propriedade

Além dos identificadores, uma propriedade é atribuída por um tipo de dados que especifica o tipo de valores permitidos para essa propriedade.
  
Para propriedades que são do tipo string, dependendo do suporte a Unicode na plataforma subjacente, a propriedade pode ser do tipo PT_STRING8 (cadeia de caracteres de 8 bits terminada em nulo) ou PT_UNICODE (string de Unicode terminada em nulo). Uma propriedade pode ser definida com o tipo PT_TSTRING e, dependendo das configurações de compilação, PT_TSTRING padrões de uma cadeia de caracteres Unicode para plataformas que dão suporte a Unicode ou uma cadeia de caracteres PT_STRING8 para plataformas que suportam ANSI ou DBCS. É comum que uma propriedade do tipo cadeia de caracteres é identificado por três nomes semelhantes, como **PR_ACCOUNT**, **PR_ACCOUNT_A**e **PR_ACCOUNT_W**, ou seja, são do tipo PT_TSTRING, PT_STRING8 e PT_UNICODE respectivamente.
  
Para obter mais informações sobre os tipos de propriedade e relacionadas a tipos de macros, consulte o arquivo de cabeçalho MAPI, Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identificar propriedades semelhantes

No cenário de propriedade MAPI atual, não é incomum para encontrar o que uma propriedade foi exposta em nomes de propriedade diferentes, todos os quais são definidos com o mesmo identificador de propriedade. Por exemplo, as propriedades marcadas, **PR_BUSINESS2_TELEPHONE_NUMBER** e **PR_OFFICE2_TELEPHONE_NUMBER**, são definidas no Mapitags.h tenham o mesmo identificador de propriedade e tipo. Intimamente relacionadas para essas duas propriedades são:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
As propriedades com o sufixo "_A" são digitadas como PT_STRING8 e aqueles com o sufixo w"são digitados como PT_UNICODE.
  
A finalidade de uma propriedade canônica, **PidTagBusiness2TelephoneNumber** neste exemplo, é facilitar referenciando dessas propriedades MAPI bastante afiliadas, usando um identificador e de forma consistente (usando o prefixo "Pid") em todos os MAPI Propriedades. Para descobrir quais propriedades MAPI reais representa uma propriedade canônica, consulte [Mapeamento canônico nomes de propriedade para nomes de MAPI](mapping-canonical-property-names-to-mapi-names.md). Para localizar a propriedade canônica que uma propriedade MAPI está associada, consulte o [Mapeamento de nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>Suporte a MAPI de nomes de propriedade canônico

Como propriedades canônicas não são propriedades real e não estão definidas em arquivos de cabeçalho MAPI, você não deve usar os nomes de propriedade canônico em código; em vez disso, você deve continuar a usar os nomes de propriedade MAPI exatos no código. Por exemplo, você pode referir-se **PR_BUSINESS2_TELEPHONE_NUMBER** e **PR_OFFICE2_TELEPHONE_NUMBER** fora do código como **PidTagBusiness2TelephoneNumber**e usar **PR_BUSINESS2_TELEPHONE_NUMBER** ou **PR_OFFICE2_ TELEPHONE_NUMBER** no código. 
  
Se você deve usar os nomes de propriedade canônico em seu código, primeiro você deve defini-los em seus próprios arquivos de cabeçalho.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Nomes de propriedade canônico e especificações de protocolo do Exchange

Nomes canônicos são referenciados nas especificações de protocolo do Microsoft Exchange Server usadas pelo Exchange Server para se comunicar com outros produtos da Microsoft. Para obter mais informações sobre propriedades de objeto de mensagem referenciado pelo especificações de protocolo do Exchange, consulte [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Confira também



[Marcas de propriedade MAPI](mapi-property-tags.md)
  
[Visão geral do identificador de propriedade MAPI](mapi-property-identifier-overview.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)

