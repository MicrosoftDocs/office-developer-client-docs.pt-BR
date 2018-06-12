---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 4fdd50a1108a6546445516664b01fb0f994fbfdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767066"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr: IUnknown

  
  
**Aplica-se a**: Outlook 
  
Permite que os visualizadores de formulário obter informações sobre e ativar servidores de formulário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de Gerenciador de formulário  <br/> |
|Implementada por:  <br/> |Provedores de biblioteca de formulário  <br/> |
|Chamado pelo:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormMgr  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Inicia um formulário para abrir uma mensagem existente.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Resolve uma classe de mensagem para o seu formulário dentro de um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Resolve um grupo de classes de mensagens para seus formulários dentro de um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Retorna uma matriz das propriedades que usa um grupo de formulários.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Inicia um formulário para criar uma nova mensagem, com base na classe de mensagem do formulário.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Apresenta uma caixa de diálogo que permite que o usuário selecione um formulário e retorna um objeto de informações de formulário que descreve nesse formulário.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Apresenta uma caixa de diálogo que permite ao usuário selecionar vários formulários e retorna uma matriz de formulário objetos de informações que descrevem esses formulários.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Apresenta uma caixa de diálogo que permite que o usuário selecione um contêiner de formulário e retorna uma interface para o objeto de contêiner do usuário selecionado.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Abre uma interface [IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Baixa um formulário para abertura.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Determina se um formulário pode lidar com conflitos sua própria mensagem.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto form manager.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

