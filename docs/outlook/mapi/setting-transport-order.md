---
title: Configurar um pedido de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 71d7ebf2bc8c7bbf3b5ee6ce60959fdeee79abe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770387"
---
# <a name="setting-transport-order"></a>Configurar um pedido de transporte

  
  
**Aplica-se a**: Outlook 
  
O MAPI spooler atribui a responsabilidade para mensagens de saída com base nos tipos de endereço e identificadores que declara, podem lidar com provedores de transporte. Provedores de transporte publicarem uma lista de tipos de endereço com suporte e os identificadores — armazenados nas estruturas **MAPIUID** — quando MAPI chama o método seus [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , diretamente após o logon. Tipo de endereço do destinatário é armazenado em sua propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Registrando para um tipo de endereço indica MAPI que o provedor de transporte que pode fornecer aos destinatários com sua propriedade **PR_ADDRTYPE** definida como o tipo de endereço registrado. Da mesma forma, se registrar para uma **MAPIUID** indica que o provedor de transporte pode fornecer aos destinatários que são representados por identificadores de entrada com o registrados **MAPIUID**.
  
A maioria dos provedores de transporte registrar para um ou mais tipos de endereço. poucos registro por **MAPIUID**. Provedores de transporte que estejam intimamente ligadas com um provedor de catálogo de endereços e entendem o seu formato de identificador de entrada podem se inscrever para lidar com as mensagens por **MAPIUID**, melhorando o desempenho. Esses provedores de transporte de ligação estreita podem extrair o endereço de email do destinatário e outras informações necessárias do identificador de entrada sem precisar abri-lo com uma chamada **IMAPISupport::OpenEntry** . 
  
MAPI mantém uma ordem para provedores de transporte, usada quando vários provedores de transporte tiverem registrado para o mesmo tipo de endereço ou **MAPIUID**. Você pode substituir essa ordem chamando [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) e passar uma lista ordenada do s **MAPIUID**de todos os provedores de transporte ativa apontado pelo parâmetro _lpUIDList_ .: 
  
Para recuperar uma lista de todos os tipos de endereço que podem ser manipulados por um dos provedores de transporte ativa, chame [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** retorna uma matriz de cadeias de caracteres que descreve os tipos de endereço suportados pelos provedores de transporte que estão ativos na sessão atual. 
  

