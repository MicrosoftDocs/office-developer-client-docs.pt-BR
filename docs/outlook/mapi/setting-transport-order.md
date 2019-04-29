---
title: Configuração da ordem de transporte
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
# <a name="setting-transport-order"></a>Configuração da ordem de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O spooler MAPI atribui responsabilidade para mensagens de saída com base nos tipos de endereço e identificadores que os provedores de transporte declaram que podem lidar. Os provedores de transporte publicam uma lista de tipos de endereço e identificadores com suporte, armazenados em estruturas **MAPIUID** , quando MAPI chama o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) , diretamente após o logon. O tipo de endereço de um destinatário é armazenado em sua propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
O registro de um tipo de endereço indica a MAPI que o provedor de transporte pode entregar aos destinatários com a propriedade **PR_ADDRTYPE** definida para o tipo de endereço registrado. Da mesma forma, registrar-se para um **MAPIUID** indica que o provedor de transporte pode entregar para destinatários representados por identificadores de entrada com o **MAPIUID**registrado.
  
A maioria dos provedores de transporte se registra para um ou mais tipos de endereço; alguns registros por **MAPIUID**. Os provedores de transporte que estão rigidamente acoplados a um provedor de catálogo de endereços e entendem seu formato de identificador de entrada podem se registrar para lidar com as mensagens por **MAPIUID**, melhorando o desempenho. Esses provedores de transporte rigidamente acoplados podem extrair o endereço de email do destinatário e outras informações necessárias do identificador de entrada sem precisar abri-lo com uma chamada **IMAPISupport:: OpenEntry** . 
  
O MAPI mantém um pedido de provedores de transporte, usado quando vários provedores de transporte foram registrados para o mesmo tipo de endereço ou **MAPIUID**. Você pode substituir esse pedido chamando [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) e passando uma lista ordenada dos **MAPIUID**s de todos os provedores de transporte ativos apontados pelo parâmetro _lpUIDList_ .: 
  
Para recuperar uma lista de todos os tipos de endereço que podem ser tratados por um dos provedores de transporte ativos, chame [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** retorna uma matriz de cadeias de caracteres que descreve os tipos de endereço suportados pelos provedores de transporte ativos na sessão atual. 
  

