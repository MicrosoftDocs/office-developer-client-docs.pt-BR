---
title: Objetos do provedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357370"
---
# <a name="mapi-transport-provider-objects"></a>Objetos do provedor de transporte MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Além dos objetos de logon e provedor padrão implementados por todos os provedores de serviços, os provedores de transporte são necessários para implementar um objeto status. Para os outros tipos de provedor de serviços, a implementação de um objeto status é opcional. No enTanto, o MAPI exige para provedores de transporte. Os provedores de transporte que dão suporte ao download de cabeçalhos de mensagens de um servidor remoto também implementam uma pasta e uma tabela. 
  
A ilustração a seguir mostra cada um dos objetos que os provedores de transporte podem implementar com suas interfaces correspondentes. A ilustração também indica se o MAPI ou um cliente é o usuário do objeto.
  
![Objetos que os provedores de transporte implementam] (media/amapi_66.gif "Objetos que os provedores de transporte implementam")
  
## <a name="see-also"></a>Confira também

- [Objetos do provedor de serviços MAPI](mapi-service-provider-objects.md)

