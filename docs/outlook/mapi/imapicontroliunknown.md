---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 80acb1a1e4663a68efc4692ab67ec27bc369f4b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566513"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Habilita e desabilita a um controle de botão e executa tarefas quando um usuário de um aplicativo cliente clica no controle habilitado. Provedores de serviço implementar objetos de controle para criar botões personalizados em caixas de diálogo, como folhas de propriedades de configuração, que são definidas por meio de tabelas de exibição. 
  
Para obter mais informações sobre como trabalhar com tabelas de exibição e controlar objetos, consulte [Exibir tabelas](display-tables.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de controle  <br/> |
|Implementada por:  <br/> |Provedores de serviços  <br/> |
|Chamado pelo:  <br/> |MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIControl  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior.  <br/> |
|[Ativar](imapicontrol-activate.md) <br/> |Executa uma tarefa como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário do aplicativo cliente clica no controle de botão.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Recupera um valor que indica se o controle de botão está ativado ou desativado.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

