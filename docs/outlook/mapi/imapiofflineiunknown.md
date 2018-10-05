---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401276"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece informações para um objeto offline.
  
|||
|:-----|:-----|
|Provided by:  <br/> |Consulta em [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Define o estado atual de um objeto offline para online ou offline.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Obtém as condições para o qual os retornos de chamada são suportados por um objeto offline.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Obtém o estado atual de online ou offline, de um objeto offline.  <br/> |
| *Membro do espaço reservado*  <br/> |Este membro é um espaço reservado e não é suportado.  <br/> |
   
## <a name="remarks"></a>Comentários

Um cliente usa **[HrOpenOfflineObj](hropenofflineobj.md)** abrir e obter um objeto offline que ofereça suporte a **IMAPIOfflineMgr**. Como **IMAPIOfflineMgr** herda de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), o cliente pode consultar a esta interface (usando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) para obter um ponteiro para o ponteiro de interface **IMAPIOffline** para o objeto offline. O cliente pode então obter ou definir o estado atual do objeto, ou Saiba mais sobre os recursos de retorno de chamada do objeto (chamando **IMAPIOffline::GetCapabilities** ) e optar por configurar retornos de chamada usando **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Um membro nesta interface é um espaço reservado reservado para uso interno do Microsoft Outlook 2013 e está sujeita a alterações. Outros membros nessa interface devem ser usados apenas como documentado. 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Interfaces MAPI](mapi-interfaces.md)

