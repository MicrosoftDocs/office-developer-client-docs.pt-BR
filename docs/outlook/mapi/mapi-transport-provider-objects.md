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
ms.openlocfilehash: de0334ee9a90da38e472571314136195c84a7866
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592700"
---
# <a name="mapi-transport-provider-objects"></a>Objetos do provedor de transporte MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Além do provedor padrão e objetos de logon implementados por todos os provedores de serviços, provedores de transporte são necessários para implementar um objeto de status. Para os outros tipos de provedor de serviço, a implementação de um objeto de status é opcional. No entanto, MAPI exige que ele para provedores de transporte. Provedores de transporte que suportam o download de cabeçalhos de mensagem de um servidor remoto também implementam uma pasta e uma tabela. 
  
A ilustração a seguir mostra cada um dos objetos que podem ser implementar provedores de transporte com suas interfaces correspondentes. A ilustração também indica se MAPI ou um cliente é o usuário do objeto.
  
![Objetos que implementam provedores de transporte] (media/amapi_66.gif "Objetos que implementam provedores de transporte")
  
## <a name="see-also"></a>Confira também

- [Objetos do provedor de serviço MAPI](mapi-service-provider-objects.md)

