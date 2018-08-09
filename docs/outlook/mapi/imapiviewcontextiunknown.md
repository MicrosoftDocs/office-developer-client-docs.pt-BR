---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a7d62253baaaae7955e722874a15d05ed16e566e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767373"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Gerencia a um formulário no Visualizador de formulário de um aplicativo cliente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Exibir objetos de contexto  <br/> |
|Implementada por:  <br/> |Visualizadores de formulário  <br/> |
|Chamado pelo:  <br/> |Objetos de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIViewContext  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Gerencia o registro de um formulário para receber notificações sobre alterações no visualizador.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Ativa a mensagem anterior ou seguinte no Visualizador do formulário.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Recupera as informações de impressão atuais.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Recupera um fluxo a ser usado para salvar a mensagem atual.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Recupera o status atual do visualizador.  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem no objeto de contexto de modo de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

