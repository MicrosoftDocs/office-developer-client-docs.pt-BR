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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321263"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece informações sobre um objeto offline.
  
|||
|:-----|:-----|
|Provided by:  <br/> |Consulta no [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|**[SetCurrentstate](imapioffline-setcurrentstate.md)** <br/> |Define o estado atual de um objeto offline para online ou offline.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Obtém as condições para as quais os retornos de chamada são compatíveis com um objeto offline.  <br/> |
|**[GetCurrentstate](imapioffline-getcurrentstate.md)** <br/> |Obtém o estado online ou offline atual de um objeto offline.  <br/> |
| *Membro PlaceHolder*  <br/> |Esse membro é um espaço reservado e não tem suporte.  <br/> |
   
## <a name="remarks"></a>Comentários

Um cliente usa **[HrOpenOfflineObj](hropenofflineobj.md)** para abrir e obter um objeto offline que oferece suporte a **IMAPIOfflineMgr**. Como o **IMAPIOfflineMgr** herda de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), o cliente pode consultar esta interface (usando [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) para obter um ponteiro para o ponteiro de interface do **IMAPIOffline** para o objeto offline. O cliente pode obter ou definir o estado atual do objeto ou descobrir sobre os recursos de retorno de chamada do objeto (chamando **IMAPIOffline:: GetCapabilities** ) e optar por configurar os retornos de chamada usando o **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Um membro desta interface é um espaço reservado reservado para o uso interno do Microsoft Outlook 2013 e está sujeito a alterações. Outros membros nesta interface devem ser usados apenas conforme documentado. 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Interfaces MAPI](mapi-interfaces.md)

