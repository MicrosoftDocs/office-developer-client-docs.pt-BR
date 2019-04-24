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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328179"
---
# <a name="mapi-property-identifier-overview"></a>Visão geral do identificador de propriedade MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um identificador de propriedade é um número que é usado para indicar o que uma propriedade é usada e quem é responsável por ela. Os identificadores de propriedade são divididos por MAPI em intervalos; onde um identificador está no intervalo indica seu uso e propriedade. 
  
O intervalo de identificadores de propriedade é executado de 0x0001 a 0xFFFF. Os identificadores de propriedade 0x0000 e 0xFFFF são reservados em todos os casos, significando que esses identificadores devem permanecer não utilizados. O intervalo de propriedades definidas por MAPI é executado de 0x0001 para 0x3FFF. Essas propriedades são referidas como propriedades definidas por MAPI. O intervalo 0x4000 a 0x7FFF pertence às propriedades message e Recipient, e os clientes ou provedores de serviços podem definir as propriedades neste intervalo. As propriedades no intervalo de 0x0001 para 0x7FFF são referidas como propriedades marcadas. Além de 0x8000 é o intervalo para o que é conhecido como propriedades nomeadas ou propriedades que incluem um identificador global exclusivo (GUID) de 32 bits e uma cadeia de caracteres Unicode ou valor numérico. Os clientes podem usar propriedades nomeadas para personalizar o conjunto de propriedades.
  
Os provedores de serviços podem definir propriedades de perfil seguras no intervalo 0x67F0 a 0x67FF. As propriedades de perfil seguro são usadas para obter informações que exijam proteção adicional, como senhas. Essas propriedades podem ser ocultas e criptografadas. Se as propriedades seguras são ou não incluídas na lista padrão de propriedades retornadas pelo método [IMAPIProp::](imapiprop-getproplist.md) getproplist depende da implementação do provedor. Normalmente, essas propriedades não são incluídas. A interface [IProfSect: IMAPIProp](iprofsectimapiprop.md) é usada para acessar as propriedades de uma seção de perfil, incluindo as propriedades seguras. 
  
Alguns dos intervalos de propriedades são restritos às propriedades transmittable ou nontransmittable. As propriedades transmittable são transferidas com uma mensagem; as propriedades nontransmittable não são transferidas com uma mensagem. As propriedades nontransmittable normalmente contêm informações que são de valor apenas para clientes e provedores de serviço que operam com a sessão atual. Essas propriedades não seriam necessariamente úteis para outro sistema de mensagens e outro conjunto de provedores de serviços. O conceito de propriedades transmittable aplica-se principalmente a provedores de transporte. Para determinar se uma propriedade é transmittable ou not, passe sua marca de propriedade para a macro **FIsTransmittable** , definida no arquivo de cabeçalho Mapitags. h. 
  
Para obter uma descrição completa dos intervalos de identificadores, consulte [Property Identifier Ranges](property-identifier-ranges.md).
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

