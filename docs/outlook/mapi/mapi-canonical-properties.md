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
  
Uma propriedade canônica é uma propriedade virtual que representa uma propriedade MAPI ou várias propriedades MAPI definidas com o mesmo identificador de propriedade. As propriedades canônicas só se destinam a facilitar a identificação consistente de propriedades MAPI em discussões ou documentação fora do código. Diferentemente dos nomes de propriedade marcados definidos por MAPI, os nomes de propriedades canônicas não são definidos como constantes globais nos arquivos de header MAPI.
  
## <a name="naming-conventions"></a>Convenções de Nomen por nome

Os nomes de propriedades canônicas começam com um prefixo, "Pid", que representa "identificador de propriedade". Dependendo se a propriedade é marcada, uma propriedade nomeada com um identificador numérico ou uma propriedade nomeada com um nome de cadeia de caracteres, o prefixo é ainda mais qualificado como "PidTag", "PidLid" e "PidName", respectivamente. Por exemplo, [PidTagAccount](pidtagaccount-canonical-property.md) representa as propriedades marcadas, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) e **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), que especificam o nome da conta de um destinatário; [PidLidContacts](pidlidcontacts-canonical-property.md) representa a **propriedade dispidContacts,** uma propriedade nomeada que tem um identificador numérico e que especifica o nome dos contatos associados a uma mensagem; e [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) representa " ," uma propriedade nomeada que tem um nome de cadeia de caracteres e que especifica as mensagens de marcação de cadeia de caracteres que provavelmente são http://schemas.microsoft.com/outlook/phishingstamp phishing. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Representando propriedades semelhantes usando uma propriedade canônica

### <a name="identifying-properties-in-mapi"></a>Identificando propriedades em MAPI

Todas as propriedades no MAPI são identificadas por um identificador de propriedade que é um valor de 16 bits não assinado. O identificador da propriedade e o tipo de propriedade (outro valor de 16 bits não assinado) constituem uma marca de propriedade para a propriedade. 
  
MAPI uses a property tag to uniquely define properties. Propriedades que têm a mesma **marca** de propriedade, como PR_BUSINESS2_TELEPHONE_NUMBER ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) e **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), são consideradas propriedades idênticas em MAPI. Para uma lista de marcas de propriedade que MAPI definiu para suas próprias propriedades, consulte o arquivo de título MAPI, Mapitags.h.
  
Observe que MAPI divide os identificadores de propriedade em intervalos. Onde um identificador cai no intervalo indica seu uso e propriedade. Os identificadores de propriedade de propriedades marcadas estão no intervalo de 0x0001 para 0x7FFF. Dentro desse intervalo estão os identificadores de propriedade de propriedades definidas por MAPI, que se enquadram no intervalo de 0x0001 para 0x3FFF. Os identificadores de propriedade de propriedades nomeadas estão no intervalo de 0x8000 a 0x8FFF. 
  
Propriedades nomeadas são atribuídas adicionalmente por um conjunto de propriedades e uma ID longa (LID), que é um valor de 32 bits não assinado ou uma cadeia de caracteres. Um conjunto de propriedades é um GUID que identifica um grupo de propriedades nomeadas com finalidade semelhante. O conjunto de propriedades e o nome da cadeia de caracteres ou LID são usados para obter ou definir a propriedade nomeada.
  
### <a name="property-type"></a>Tipo de propriedade

Além dos identificadores, uma propriedade é atribuída por um tipo de dados que especifica os tipos de valores permitidos para essa propriedade.
  
Para propriedades que são do tipo de cadeia de caracteres, dependendo do suporte para Unicode na plataforma subjacente, a propriedade pode ser do tipo PT_STRING8 (cadeia de caracteres terminada por caractere nulo de 8 bits) ou PT_UNICODE (cadeia de caracteres Unicode terminada por caractere nulo). Uma propriedade pode ser definida com o tipo PT_TSTRING e, dependendo das configurações de compilação, o PT_TSTRING assume como padrão uma cadeia de caracteres Unicode para plataformas que suportam Unicode ou uma cadeia de caracteres PT_STRING8 para plataformas que suportam ANSI ou DBCS. É comum que uma propriedade de cadeia de caracteres digitada seja identificada por três nomes semelhantes, como **PR_ACCOUNT**, **PR_ACCOUNT_A** e **PR_ACCOUNT_W**, que são do tipo PT_TSTRING, PT_STRING8 e PT_UNICODE respectivamente.
  
Para obter mais informações sobre tipos de propriedade e macros relacionadas a tipos, consulte o arquivo de header MAPI, Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identificando propriedades semelhantes

No cenário de propriedades MAPI atual, não é incomum descobrir que uma propriedade foi exposta em nomes de propriedades diferentes, todos definidos com o mesmo identificador de propriedade. Por exemplo, as propriedades marcadas, **PR_BUSINESS2_TELEPHONE_NUMBER** e **PR_OFFICE2_TELEPHONE_NUMBER**, são definidas em Mapitags.h para ter o mesmo identificador e tipo de propriedade. Intimamente relacionados a essas duas propriedades são:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
As propriedades com o sufixo "_A" são digitadas como PT_STRING8 e as com o sufixo "_W" são digitadas como PT_UNICODE.
  
O objetivo de uma propriedade canônica, **PidTagBusiness2TelephoneNumber** neste exemplo, é facilitar a referência a essas propriedades MAPI associadas de forma próxima usando um identificador e de forma consistente (usando o prefixo "Pid" ) em todas as propriedades MAPI. Para descobrir quais propriedades MAPI reais uma propriedade canônica representa, consulte Mapeamento de nomes de propriedades [canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md). Para encontrar a propriedade canônica à que uma propriedade MAPI está associada, consulte Mapeamento de nomes MAPI para nomes [de propriedade canônica.](mapping-mapi-names-to-canonical-property-names.md)
  
## <a name="mapi-support-of-canonical-property-names"></a>Suporte MAPI de nomes de propriedades canônicas

Como as propriedades canônicas não são propriedades reais e não são definidas em arquivos de header MAPI, você não deve usar nomes de propriedade canônica em código; em vez disso, você deve continuar a usar os nomes de propriedade MAPI exatos no código. Por exemplo, você  pode fazer referência PR_BUSINESS2_TELEPHONE_NUMBER e **PR_OFFICE2_TELEPHONE_NUMBER** fora do código como **PidTagBusiness2TelephoneNumber** e usar PR_BUSINESS2_TELEPHONE_NUMBER ou **PR_OFFICE2_TELEPHONE_NUMBER** em código.  
  
Se for necessário usar nomes de propriedades canônicas em seu código, você deve defini-los primeiro em seus próprios arquivos de título.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Nomes de propriedades canônicas e especificações de protocolo do Exchange

Os nomes canônicos são referenciados nas especificações de protocolo do Microsoft Exchange Server usadas pelo Exchange Server para se comunicar com outros produtos da Microsoft. Para obter mais informações sobre as propriedades do objeto de mensagem referenciadas pelas especificações de protocolo do Exchange, consulte [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Confira também



[Marcas de propriedade MAPI](mapi-property-tags.md)
  
[Visão geral do identificador de propriedade MAPI](mapi-property-identifier-overview.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)

