---
title: Visão geral do identificador de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 29626f49365a0f37f1e13d965c62bfd5ad0fb774
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414694"
---
# <a name="mapi-property-identifier-overview"></a>Visão geral do identificador de propriedade MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um identificador de propriedade é um número usado para indicar para que uma propriedade é usada e quem é responsável por ela. Os identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador está no intervalo indica seu uso e propriedade. 
  
O intervalo de identificadores de propriedade é executado 0x0001 a 0xFFFF. Os identificadores 0x0000 e 0xFFFF são reservados em todos os casos, o que significa que esses identificadores devem permanecer não sendousados. O intervalo para propriedades definidas por MAPI é executado 0x0001 a 0x3FFF. Essas propriedades são conhecidas como propriedades definidas por MAPI. O intervalo 0x4000 a 0x7FFF pertence às propriedades de mensagem e destinatário, e clientes ou provedores de serviços podem definir propriedades nesse intervalo. Propriedades no intervalo de 0x0001 a 0x7FFF são referidas como propriedades marcadas. Além 0x8000 é o intervalo para o que é conhecido como propriedades nomeadas ou propriedades que incluem um identificador global exclusivo (GUID) de 32 bits e um valor numérico ou cadeia de caracteres Unicode. Os clientes podem usar propriedades nomeadas para personalizar o conjunto de propriedades.
  
Os provedores de serviços podem definir propriedades de perfil seguras no intervalo 0x67F0 por meio 0x67FF. Propriedades de perfil seguro são usadas para informações que exigem proteção adicional, como senhas. Essas propriedades podem ser ocultas e criptografadas. Se as propriedades seguras são incluídas ou não na lista padrão de propriedades retornadas pelo método [IMAPIProp::GetPropList](imapiprop-getproplist.md) depende da implementação do provedor. Geralmente, essas propriedades não são incluídas. A interface [IProfSect : IMAPIProp](iprofsectimapiprop.md) é usada para acessar as propriedades de uma seção de perfil, incluindo propriedades seguras. 
  
Alguns dos intervalos de propriedades são restritos a propriedades transmitíveis ou propriedades nãotransmitíveis. As propriedades transmitíveis são transferidas com uma mensagem; propriedades nãotransmitíveis não são transferidas com uma mensagem. Propriedades nãotransmitíveis geralmente contêm informações que são de valor apenas para clientes e provedores de serviços que operam com a sessão atual. Essas propriedades não seriam necessariamente úteis para outro sistema de mensagens e outro conjunto de provedores de serviços. O conceito de propriedades transmitíveis se aplica principalmente a provedores de transporte. Para determinar se uma propriedade é transmitível ou não, passe sua marca de propriedade para a macro **FIsTransmittable,** definida no arquivo de título Mapitags.h. 
  
Para uma descrição completa dos intervalos de identificador, consulte [Intervalos de Identificador de Propriedade.](property-identifier-ranges.md)
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

