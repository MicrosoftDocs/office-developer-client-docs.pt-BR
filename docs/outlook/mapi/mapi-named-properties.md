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
ms.openlocfilehash: 5a6ba7af5e497ba59b43e9b80cfc9595961ed10e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579540"
---
# <a name="mapi-named-properties"></a>MAPI denominada propriedades
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI fornece uma facilidade para atribuir nomes às propriedades, para mapear esses nomes para identificadores exclusivos e para tornar esse mapeamento persistente. Nome persistente para mapeamento do identificador garante que os nomes de propriedade permaneçam válidos nas sessões.
  
Para definir uma propriedade nomeada, um provedor de cliente ou serviço constitui um nome e o armazena em uma estrutura [MAPINAMEID](mapinameid.md) . Porque nomes são compostos de um identificador globalmente exclusivo de 32 bits, ou GUID e qualquer um Unicode caractere cadeia de caracteres ou um valor numérico, os criadores de propriedades nomeadas podem criar nomes significativos sem medo de duplicação. Nomes são exclusivos e eles podem ser usados sem relação com o valor dos seus identificadores. 
  
Para oferecer suporte a propriedades nomeadas, um provedor de serviço implementa dois métodos — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — convertem entre nomes e os identificadores e permitir seu [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) métodos para recuperar e modificar as propriedades com identificadores no intervalo nomeado de propriedade. O intervalo para identificadores de propriedade nomeada é entre 0x8000 e 0xFFFE. 
  
Qualquer objeto que implementa a interface **IMAPIProp** pode oferecer suporte a propriedades nomeadas. Provedores de catálogo de endereços que permitem que as entradas de outros provedores a serem copiados para seus contêineres e mensagem armazenam provedores que podem ser usados para criar tipos de mensagem arbitrária são necessários para fornecer esse suporte. É uma opção para todos os outros provedores de serviços. Provedores que não oferecem suporte a propriedades nomeadas retornam MAPI_E_NO_SUPPORT dos métodos **GetIDsFromNames** e **GetNamesFromIDs** e se recusar a definir todas as propriedades com identificadores de 0x8000 ou posterior, retornando MAPI_E_UNEXPECTED no ** SPropProblemarray**.
  
A criação de nomes de propriedades é uma maneira para que os clientes definir novas propriedades para classes de mensagem existente ou personalizado. Provedores de serviço podem usar propriedades nomeadas expor recursos exclusivos de seus sistemas de mensagens. Ainda é outro uso de propriedades nomeadas oferecer uma maneira alternativa de se referir a propriedades com identificadores abaixo 0x8000. 
  
Por exemplo, um cliente poderia usar código semelhante ao seguinte código para recuperar os nomes de todas as propriedades de um objeto nomeado:
  
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

Para solicitar todos os nomes de conjunto de propriedades PS_PUBLIC_STRINGS, um cliente substituiria o NULL no parâmetro propriedade set para PS_PUBLIC_STRINGS da seguinte maneira: 
  
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

