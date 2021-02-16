---
title: Configurando a ordem de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433595"
---
# <a name="setting-transport-order"></a>Configurando a ordem de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O spooler MAPI atribui responsabilidade por mensagens de saída com base nos tipos de endereço e identificadores que os provedores de transporte declaram que podem manipular. Os provedores de transporte publicam uma lista de tipos de endereços e identificadores com suporte — armazenados em estruturas **MAPIUID** — quando o MAPI chama seu método [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) diretamente após o logon. O tipo de endereço de um destinatário é armazenado **em sua PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) .
  
O registro de um tipo de endereço indica ao MAPI que o provedor de transporte pode entregar aos destinatários com a propriedade **PR_ADDRTYPE** definida como o tipo de endereço registrado. Da mesma forma, registrar-se para um **MAPIUID** indica que o provedor de transporte pode entregar aos destinatários representados por identificadores de entrada com **MAPIUID registrado.**
  
A maioria dos provedores de transporte se registra para um ou mais tipos de endereços; alguns se registram **por MAPIUID**. Os provedores de transporte que estão fortemente unidos a um provedor de agendamento de endereços e entendem seu formato de identificador de entrada podem se registrar para manipular mensagens por **MAPIUID,** melhorando assim o desempenho. Esses provedores de transporte fortemente aparados podem extrair o endereço de email do destinatário e outras informações necessárias do identificador de entrada sem precisar abri-lo com uma chamada **IMAPISupport::OpenEntry.** 
  
MAPI mantém uma ordem para provedores de transporte, usado quando vários provedores de transporte foram registrados para o mesmo tipo de endereço ou **MAPIUID**. Você pode substituir essa ordem chamando [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) e passando uma lista ordenada de **MAPIUID** s de todos os provedores de transporte ativos apontados pelo parâmetro _lpUIDList.:_ 
  
Para recuperar uma lista de todos os tipos de endereços que podem ser manipulados por um dos provedores de transporte ativos, chame [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** retorna uma matriz de cadeias de caracteres que descreve os tipos de endereços suportados pelos provedores de transporte que estão ativos na sessão atual. 
  

