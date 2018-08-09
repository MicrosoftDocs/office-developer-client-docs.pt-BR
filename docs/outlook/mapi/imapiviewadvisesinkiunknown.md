---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767352"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Recebe notificações de formulários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de coletor de eventos de aviso do modo de exibição  <br/> |
|Implementada por:  <br/> |Visualizadores de formulário  <br/> |
|Chamado pelo:  <br/> |Objetos de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Notifica o Visualizador de formulário que um formulário está sendo fechado.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Notifica o Visualizador de formulário que uma mensagem existente ou um novo foi carregada em um formulário.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Notifica o Visualizador de formulário do status impressão de um formulário.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Notifica o Visualizador de formulário que a mensagem atual foi enviada para o spooler MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Notifica o Visualizador de formulário que tenha sido salva a mensagem atual em um formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

