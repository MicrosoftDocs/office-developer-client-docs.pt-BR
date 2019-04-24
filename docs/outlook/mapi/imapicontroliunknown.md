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
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280138"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Habilita e desabilita um controle de botão e realiza tarefas quando um usuário de um aplicativo cliente clica no controle habilitado. Os provedores de serviços implementam objetos de controle para criar botões personalizados em caixas de diálogo, como as folhas de propriedades de configuração, que são definidas usando as tabelas de exibição. 
  
Para obter mais informações sobre como trabalhar com tabelas de exibição e objetos de controle, consulte [Exibir tabelas](display-tables.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos de controle  <br/> |
|Implementado por:  <br/> |Provedores de serviços  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIControl  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior.  <br/> |
|[Ativar](imapicontrol-activate.md) <br/> |Executa uma tarefa, como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário de aplicativo cliente clica no controle de botão.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Recupera um valor que indica se o controle de botão está habilitado ou desabilitado.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

