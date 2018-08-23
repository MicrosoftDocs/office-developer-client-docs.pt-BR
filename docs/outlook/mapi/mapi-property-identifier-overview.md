---
title: Visão geral do identificador de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8cf2f08a69ee87c40789b764596e514c91483c2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563153"
---
# <a name="mapi-property-identifier-overview"></a>Visão geral do identificador de propriedade MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um identificador de propriedade é um número que é usado para indicar que uma propriedade é usada e quem é responsável por ela. Identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador cai no intervalo indica seu uso e a propriedade. 
  
O intervalo de identificadores de propriedade executa a partir 0x0001 através de 0xFFFF. Identificadores de propriedade 0x0000 e 0xFFFF são reservados em todos os casos, o que significa que esses identificadores devem permanecer não utilizados. O intervalo para propriedades definidas pelo MAPI executa a partir 0x0001 para 0x3FFF. Essas propriedades são chamadas de propriedades definidas pelo MAPI. O intervalo 0x4000 para 0x7FFF pertence a mensagem e propriedades de destinatário e clientes ou provedores de serviços podem definir as propriedades nesse intervalo. Propriedades no intervalo de 0x0001 para 0x7FFF são chamadas de propriedades marcadas. Além de 0x8000 é o intervalo para o que é conhecido como propriedades nomeadas ou propriedades que incluem um identificador globalmente exclusivo (GUID) de 32 bits e uma cadeia de caracteres Unicode ou valor numérico. Clientes podem usar propriedades nomeadas para personalizar seu conjunto de propriedades.
  
Provedores de serviços podem definir propriedades de perfil segura no intervalo 0x67F0 por meio de 0x67FF. Proteja as propriedades são usadas para informações que exigem proteção adicional, como senhas de perfil. Essas propriedades podem ser ocultadas e criptografadas. Ou não as propriedades seguras estão incluídas na lista padrão de propriedades retornadas pelo método [IMAPIProp::GetPropList](imapiprop-getproplist.md) dependem da implementação do provedor. Geralmente, essas propriedades não são incluídas. O [IProfSect: IMAPIProp](iprofsectimapiprop.md) interface é usada para acessar as propriedades de uma seção de perfil, incluindo propriedades seguras. 
  
Alguns dos intervalos de propriedade são restritos a propriedades transmittable ou nontransmittable. Propriedades transmittable são transferidas com uma mensagem; Propriedades de nontransmittable não são transferidas com uma mensagem. Propriedades de Nontransmittable geralmente contêm informações do valor somente a clientes e provedores de serviços operacional com a sessão atual. Essas propriedades não necessariamente seria útil para outro sistema de mensagens e outro conjunto de provedores de serviço. O conceito de propriedades transmittable aplica-se principalmente para provedores de transporte. Para determinar se uma propriedade é transmittable ou não, passe a marca de sua propriedade à macro **FIsTransmittable** , definida no arquivo de cabeçalho Mapitags.h. 
  
Para obter uma descrição completa dos intervalos identificador, consulte [Intervalos de identificador de propriedade](property-identifier-ranges.md).
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

