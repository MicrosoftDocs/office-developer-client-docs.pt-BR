---
title: Objetos de provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430354"
---
# <a name="mapi-transport-provider-objects"></a>Objetos de provedor de transporte MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Além do provedor padrão e dos objetos de logon implementados por todos os provedores de serviços, os provedores de transporte são necessários para implementar um objeto de status. Para os outros tipos de provedores de serviços, implementar um objeto de status é opcional. No entanto, o MAPI exige isso para provedores de transporte. Os provedores de transporte que suportam o download de headers de mensagens de um servidor remoto também implementam uma pasta e uma tabela. 
  
A ilustração a seguir mostra cada um dos objetos que os provedores de transporte podem implementar com suas interfaces correspondentes. A ilustração também indica se MAPI ou um cliente é o usuário do objeto.
  
![Objetos que os provedores de transporte implementam](media/amapi_66.gif "Objetos que os provedores de transporte implementam")
  
## <a name="see-also"></a>Confira também

- [Objetos do provedor de serviços MAPI](mapi-service-provider-objects.md)

