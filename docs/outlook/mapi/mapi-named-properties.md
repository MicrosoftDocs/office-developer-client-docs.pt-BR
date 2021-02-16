---
title: MAPI denominada propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435044"
---
# <a name="mapi-named-properties"></a>MAPI denominada propriedades
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent. O nome persistente do mapeamento de identificador garante que os nomes de propriedade permaneçam válidos entre sessões.
  
Para definir uma propriedade nomeada, um cliente ou provedor de serviços com um nome e o armazena em uma [estrutura MAPINAMEID.](mapinameid.md) Como os nomes são feitos de um identificador global exclusivo de 32 bits ou GUID e uma cadeia de caracteres Unicode ou um valor numérico, os criadores de propriedades nomeadas podem criar nomes significativos sem o medo da duplicação. Os nomes são exclusivos e podem ser usados sem considerar o valor de seus identificadores. 
  
Para dar suporte a propriedades nomeadas, um provedor de serviços implementa dois métodos [— IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — para traduzir entre nomes e identificadores e permitir que seus métodos [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) recuperem e modifiquem propriedades com identificadores no intervalo de propriedades nomeados. O intervalo para identificadores de propriedade nomeados é 0x8000 e 0xFFFE. 
  
Qualquer objeto que implemente a interface **IMAPIProp** pode dar suporte a propriedades nomeadas. Provedores de agendas que permitem que entradas de outros provedores sejam copiadas para seus contêineres e provedores de armazenamento de mensagens que podem ser usados para criar tipos de mensagem arbitrários são necessários para fornecer esse suporte. É uma opção para todos os outros provedores de serviços. Provedores que não suportam propriedades nomeadas retornam MAPI_E_NO_SUPPORT dos métodos **GetIDsFromNames** e **GetNamesFromIDs** e se recusam a definir quaisquer propriedades com identificadores de 0x8000 ou superior, retornando MAPI_E_UNEXPECTED no **SPropProblemarray**.
  
Criar nomes para propriedades é uma maneira dos clientes definirem novas propriedades para classes de mensagens existentes ou personalizadas. Os provedores de serviços podem usar propriedades nomeadas para expor recursos exclusivos de seus sistemas de mensagens. Ainda assim, outro uso para propriedades nomeadas é fornecer uma maneira alternativa de se referir a propriedades com identificadores abaixo 0x8000. 
  
Por exemplo, um cliente poderia usar código semelhante ao código a seguir para recuperar os nomes de todas as propriedades nomeadas de um objeto:
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

Para solicitar todos os nomes do conjunto PS_PUBLIC_STRINGS propriedade, um cliente substituiria NULL no parâmetro do conjunto de propriedades para PS_PUBLIC_STRINGS da seguinte forma: 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

