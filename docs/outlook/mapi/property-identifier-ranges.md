---
title: Intervalos do Identificador de Propriedade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422702"
---
# <a name="property-identifier-ranges"></a>Intervalos do Identificador de Propriedade

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela a seguir resume os diferentes intervalos de identificadores de propriedade, descrevendo o proprietário das propriedades em cada intervalo.
  
|**Intervalo de identificadores**|**Descrição**|
|:-----|:-----|
|0000  <br/> |Reservado por MAPI para o valor especial **PR_NULL**.  <br/> |
|0001 - 0BFF  <br/> |Propriedades de envelope de mensagem definidas por MAPI.  <br/> |
|0C00 - 0DFF  <br/> |Propriedades de destinatário definidas por MAPI.  <br/> |
|0E00 - 0FFF  <br/> |Propriedades de mensagens não transmitíveis definidas por MAPI.  <br/> |
|1000 - 2FFF  <br/> |Propriedades de conteúdo de mensagens definidas por MAPI.  <br/> |
|3000 - 3FFF  <br/> |Propriedades para objetos diferentes de mensagens e destinatários definidos por MAPI.  <br/> |
|4000 - 57FF  <br/> |Propriedades de envelope de mensagem definidas pelos provedores de transporte.  <br/> |
|5800 - 5FFF  <br/> |Propriedades de destinatário definidas pelos provedores de transporte e de agenda de endereços.  <br/> |
|6000 - 65FF  <br/> |Propriedades de mensagens não transmitíveis definidas pelos clientes.  <br/> |
|6600 - 67FF  <br/> |Propriedades não transmitíveis definidas por um provedor de serviços. Essas propriedades podem ser visíveis ou invisíveis para os usuários.  <br/> |
|6800 - 7BFF  <br/> |Propriedades de conteúdo de mensagens para classes de mensagens personalizadas definidas pelos criadores dessas classes.  <br/> |
|7C00 - 7FFF  <br/> |Propriedades não transmitíveis para classes de mensagens personalizadas definidas pelos criadores dessas classes.  <br/> |
|8000 - FFFE  <br/> |Propriedades definidas por clientes e, ocasionalmente, provedores de serviços identificados por nome por meio dos métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)  <br/> |
|FFFF  <br/> |Reservado por MAPI para o valor de erro especial PROP_ID_INVALID.  <br/> |
   
O intervalo entre 3000 e 3FFF é reservado para propriedades que não estão relacionadas a mensagens ou destinatários. MAPI divide esse intervalo em sub-intervalos por tipos de objeto; a tabela a seguir mostra essa divisão posterior. 
  
|**Intervalo de identificadores**|**Tipo de propriedade**|
|:-----|:-----|
|3000 - 33FF  <br/> |Propriedades comuns que aparecem em vários objetos, como **PR_DISPLAY_NAME** e **PR_ENTRYID**.  <br/> |
|3400 - 35FF  <br/> |Propriedades do armazenamento de mensagens  <br/> |
|3600 - 36FF  <br/> |Propriedades do contêiner da pasta e do livro de endereços  <br/> |
|3700 - 38FF  <br/> |Propriedades de anexo  <br/> |
|3900 - 39FF  <br/> |Propriedades do livro de endereços  <br/> |
|3A00 - 3BFF  <br/> |Propriedades do usuário de mensagens  <br/> |
|3C00 - 3CFF  <br/> |Propriedades da lista de distribuição  <br/> |
|3D00 - 3DFF  <br/> |Propriedades de perfil  <br/> |
|3E00 - 3FFF  <br/> |Propriedades do objeto Status  <br/> |
   

