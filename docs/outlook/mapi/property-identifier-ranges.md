---
title: Intervalos de identificador de propriedade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328529"
---
# <a name="property-identifier-ranges"></a>Intervalos de identificador de propriedade

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela a seguir resume os diferentes intervalos de identificadores de propriedade, descrevendo o proprietário das propriedades em cada intervalo.
  
|**Intervalo de identificador**|**Descrição**|
|:-----|:-----|
|0000  <br/> |Reservado por MAPI para o valor especial **PR_NULL**.  <br/> |
|0001-0BFF  <br/> |Propriedades de envelope de mensagem definidas por MAPI.  <br/> |
|0C00-0DFF  <br/> |Propriedades de destinatário definidas por MAPI.  <br/> |
|0E00-0FFF  <br/> |Propriedades de mensagens que não são de transmittable definidas por MAPI.  <br/> |
|1000-2FFF  <br/> |Propriedades de conteúdo da mensagem definidas por MAPI.  <br/> |
|3000-3FFF  <br/> |Propriedades de objetos diferentes de mensagens e destinatários definidos por MAPI.  <br/> |
|4000-57FF  <br/> |Propriedades de envelope de mensagem definidas por provedores de transporte.  <br/> |
|5800-5FFF  <br/> |Propriedades do destinatário definidas por provedores de transporte e catálogo de endereços.  <br/> |
|6000-65FF  <br/> |Propriedades de mensagens que não são de transmittable definidas por clientes.  <br/> |
|6600-67FF  <br/> |Propriedades que não são de transmittable definidas por um provedor de serviços. Essas propriedades podem ser visíveis ou invisíveis aos usuários.  <br/> |
|6800-7BFF  <br/> |Propriedades de conteúdo da mensagem para classes de mensagens personalizadas definidas pelos criadores dessas classes.  <br/> |
|7C00-7FFF  <br/> |Propriedades não transmittable para classes de mensagens personalizadas definidas pelos criadores dessas classes.  <br/> |
|8000-FFFE  <br/> |Propriedades definidas por clientes e provedores de serviços ocasionalmente identificados por nome pelos métodos [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .  <br/> |
|FFF  <br/> |Reservado por MAPI para o valor de erro especial PROP_ID_INVALID.  <br/> |
   
O intervalo entre 3000 e 3FFF é reservado para propriedades que não estão relacionadas a mensagens ou destinatários. O MAPI divide esse intervalo em subintervalos por tipos de objeto; a tabela a seguir mostra essa divisão adicional. 
  
|**Intervalo de identificador**|**Tipo de propriedade**|
|:-----|:-----|
|3000-33FF  <br/> |Propriedades comuns que aparecem em vários objetos, como **PR_DISPLAY_NAME** e **PR_ENTRYID**.  <br/> |
|3400-35FF  <br/> |Propriedades do repositório de mensagens  <br/> |
|3600-36FF  <br/> |Propriedades do contêiner de pasta e catálogo de endereços  <br/> |
|3700-38FF  <br/> |Propriedades do anexo  <br/> |
|3900-39FF  <br/> |Propriedades do catálogo de endereços  <br/> |
|3A00-3BFF  <br/> |Propriedades do usuário de mensagens  <br/> |
|3C00-3CFF  <br/> |Propriedades da lista de distribuição  <br/> |
|3D00-3DFF  <br/> |Propriedades de perfil  <br/> |
|3E00-3FFF  <br/> |Propriedades do objeto status  <br/> |
   

