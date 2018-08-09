---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: f4b57ad1062df9aa1809e8eb422a2c983adcac4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765980"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Fornece um retorno de chamada para o cliente para que as alterações a uma conta.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Provided by:  <br/> | Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |Notifica o cliente de alterações para a conta especificada.  <br/> |
   
## <a name="remarks"></a>Comentários

Esta interface é passado para [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) quando Configurando notificações. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

