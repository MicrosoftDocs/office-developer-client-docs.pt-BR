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
ms.openlocfilehash: 644fad96c8aec3701233351469a84ef93341b397
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767137"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Aplica-se a**: Outlook 
  
Suporta Registrando para retornos de chamada de notificação sobre alterações de estado de conexão de uma conta de usuário.
  
|||
|:-----|:-----|
|Exportá-los por:  <br/> |Msmapi32  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Aviso](imapiofflinemgr-advise.md) <br/> |Registra para retornos de chamada de notificação sobre alterações de conexão.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Remove um determinado registro para retornos de chamada de notificação.  <br/> |
| *Membro do espaço reservado*  <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
| *Membro do espaço reservado*  <br/> | *Este membro é um espaço reservado e não é suportado.*  <br/> |
   
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline para um perfil de conta de usuário usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente obtém um objeto offline que suporta **IMAPIOfflineMgr**. 
  
Como essa interface herda de **[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)**, o cliente pode consultar a esta interface (usando **[IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)** ) para obter um objeto que ofereça suporte a **[IMAPIOffline](imapiofflineiunknown.md)**. O cliente pode saber sobre os recursos de retorno de chamada do objeto offline (por chamada **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ) e optar por configurar retornos de chamada (usando **IMAPIOfflineMgr::Advise** ). 
  
A maioria dos membros nessa interface é espaços reservados reservados para uso interno do Outlook e está sujeita a alterações. Os chamadores dessa interface devem usar membros sem placeholder apenas conforme documentado.
  
## <a name="see-also"></a>Confira também



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Interfaces MAPI](mapi-interfaces.md)

