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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413056"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que os visualizadores de formulário obtenham informações sobre e ativem servidores de formulário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Exposto por:  <br/> |Objetos do gerenciador de formulário  <br/> |
|Implementado por:  <br/> |Provedores de biblioteca de formulário  <br/> |
|Chamado por:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormMgr  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Inicia um formulário para abrir uma mensagem existente.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Resolve uma classe de mensagem para seu formulário dentro de um contêiner de formulário e retorna um objeto de informações de formulário para esse formulário.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Resolve um grupo de classes de mensagem para seus formulários dentro de um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Retorna uma matriz das propriedades que um grupo de formulários usa.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Inicia um formulário para criar uma nova mensagem com base na classe de mensagem do formulário.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Apresenta uma caixa de diálogo que permite ao usuário selecionar um formulário e retorna um objeto de informações de formulário que descreve esse formulário.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Apresenta uma caixa de diálogo que permite ao usuário selecionar vários formulários e retorna uma matriz de objetos de informações de formulário que descrevem esses formulários.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Apresenta uma caixa de diálogo que permite ao usuário selecionar um contêiner de formulário e retorna uma interface para o objeto contêiner selecionado pelo usuário.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Abre uma [interface IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Baixa um formulário para abertura.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Determina se um formulário pode lidar com seus próprios conflitos de mensagem.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior ocorrendo no objeto gerenciador de formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

