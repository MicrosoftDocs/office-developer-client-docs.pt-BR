---
title: Intervalos do identificador de propriedades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 479e5abda9137ddaedcabb8d914bc038ddf200f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581101"
---
# <a name="property-identifier-ranges"></a>Intervalos do identificador de propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela a seguir resume os diferentes intervalos para os identificadores de propriedade, descrevendo o proprietário para as propriedades em cada intervalo.
  
|**Intervalo de identificador**|**Descrição**|
|:-----|:-----|
|0000  <br/> |Reservado pelo MAPI para o valor especial **PR_NULL**.  <br/> |
|0001 - 0BFF  <br/> |Propriedades de envelope de mensagem definidas por MAPI.  <br/> |
|0C 00 - 0DFF  <br/> |Propriedades de destinatário definidas pela MAPI.  <br/> |
|0E00 - 0FFF  <br/> |Propriedades de mensagem não-transmittable definidas por MAPI.  <br/> |
|1000 - 2FFF  <br/> |Propriedades do conteúdo de mensagem definidas por MAPI.  <br/> |
|3000 - 3FFF  <br/> |Propriedades de objetos que não sejam mensagens e destinatários definidos pelo MAPI.  <br/> |
|4000 - 57FF  <br/> |Propriedades de envelope de mensagem definidas por provedores de transporte.  <br/> |
|5800 - 5FFF  <br/> |Propriedades de destinatário definidas pelos provedores de catálogo de endereço e transporte.  <br/> |
|6000 - 65FF  <br/> |Propriedades de mensagem não-transmittable definidas por clientes.  <br/> |
|6600 - 67FF  <br/> |Propriedades de não-transmittable definidas por um provedor de serviços. Essas propriedades podem ser visíveis ou invisíveis aos usuários.  <br/> |
|6800 - 7BFF  <br/> |Propriedades de conteúdo de mensagem para classes de mensagem personalizada definidas pelo criadores dessas classes.  <br/> |
|7C 00 - 7FFF  <br/> |Propriedades não-transmittable de classes de mensagem personalizada definidas por criadores dessas classes.  <br/> |
|8000 - FFFE  <br/> |Propriedades definidas pelos clientes e ocasionalmente provedores identificados pelo nome, por meio dos métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) de serviços.  <br/> |
|FFFF  <br/> |Reservado pelo MAPI para o valor de erro especial PROP_ID_INVALID.  <br/> |
   
O intervalo entre 3000 e 3FFF é reservado para propriedades que não estão relacionadas a mensagens ou destinatários. MAPI divide esse intervalo em intervalos sub-recurso por tipos de objeto; a tabela a seguir mostra este obter informações mais detalhadas. 
  
|**Intervalo de identificador**|**Tipo de propriedade**|
|:-----|:-----|
|3000 - 33FF  <br/> |Propriedades comuns que aparecem em vários objetos, como **PR_DISPLAY_NAME** e **PR_ENTRYID**.  <br/> |
|3400 - 35FF  <br/> |Repositório de propriedades da mensagem  <br/> |
|3600 - 36FF  <br/> |Propriedades de contêiner do catálogo de endereços e de pasta  <br/> |
|3700 - 38FF  <br/> |Propriedades de anexo  <br/> |
|3900 - 39FF  <br/> |Propriedades do catálogo de endereços  <br/> |
|3A00 - 3BFF  <br/> |Propriedades do usuário de mensagens  <br/> |
|3C 00 - E 3CFF  <br/> |Propriedades da lista de distribuição  <br/> |
|3D 00 - 3DFF  <br/> |Propriedades de perfil  <br/> |
|3E00 - 3FFF  <br/> |Propriedades do objeto de status  <br/> |
   

