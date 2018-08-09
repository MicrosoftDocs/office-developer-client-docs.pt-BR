---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 3c28b1e8ab7e2d72d27cc6545b6ef57834ef5b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765949"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Fornece a funcionalidade de auxiliar na sessão MAPI atual para gerenciar contas.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Provided by:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Obtém o nome do perfil de uma conta.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Abre uma sessão MAPI e mantém uma referência para a sessão para o gerente de conta.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Libera o objeto de sessão MAPI que foi retornado por [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Comentários

Esta interface é passado para [IOlkAccountManager::Init](iolkaccountmanager-init.md) ao inicializar o Gerenciador de conta. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

