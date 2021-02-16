---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 235c2afb20e6f36df72eac4070c1df5fd10fcce8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270088"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oferece suporte ao registro para retornos de chamada de notificação sobre alterações de estado de conexão de uma conta de usuário.
  
|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Advise](imapiofflinemgr-advise.md) <br/> |Registra retornos de chamada de notificação sobre alterações de conexão.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Remove um determinado registro para retornos de chamada de notificação.  <br/> |
| *Membro placeholder*  <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
| *Membro placeholder*  <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
| *Membro placeholder*  <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
| *Membro placeholder*  <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
| *Membro placeholder*  <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
| *Membro placeholder*  <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
| *Membro placeholder*  <br/> | *Esse membro é um espaço reservado e não tem suporte.*  <br/> |
   
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline para um perfil de conta de usuário usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente obtém um objeto offline que dá suporte a **IMAPIOfflineMgr**. 
  
Como essa interface herda de **[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)**, o cliente pode consultar essa interface (usando **[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** ) para obter um objeto que dá suporte a **[IMAPIOffline](imapiofflineiunknown.md)**. Em seguida, o cliente pode descobrir os recursos de retorno de chamada do objeto offline (chamando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ) e optar por configurar retornos de chamada (usando **IMAPIOfflineMgr::Advise** ). 
  
A maioria dos membros dessa interface consiste em espaços reservados para uso interno do Outlook e está sujeita a alterações. Os chamadores desta interface devem usar membros que não são de espaço reservado somente conforme documentado.
  
## <a name="see-also"></a>Confira também



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Interfaces MAPI](mapi-interfaces.md)

