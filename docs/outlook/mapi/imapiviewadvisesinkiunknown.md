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
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429415"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recebe notificações de formulários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Exposto por:  <br/> |Exibir objetos de aconselhá-os  <br/> |
|Implementado por:  <br/> |Visualizadores de formulário  <br/> |
|Chamado por:  <br/> |Objetos de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Notifica o visualizador de formulário de que um formulário está sendo fechado.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Notifica o visualizador de formulário de que uma mensagem nova ou existente foi carregada em um formulário.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Notifica o visualizador de formulário sobre o status de impressão de um formulário.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Notifica o visualizador de formulário de que a mensagem atual foi enviada para o spooler MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Notifica o visualizador de formulário de que a mensagem atual em um formulário foi salva.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

