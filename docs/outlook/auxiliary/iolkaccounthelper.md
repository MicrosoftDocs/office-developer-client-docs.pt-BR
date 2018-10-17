---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386408"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Fornece funcionalidade de ajuda na sessão MAPI atual para gerenciar contas.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fornecido por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Obtém o nome de um perfil de conta.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Lança o objeto de sessão MAPI retornado por [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Comentários

Essa interface é passada para [IOlkAccountManager::Init](iolkaccountmanager-init.md) ao inicializar o gerente de contas. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

