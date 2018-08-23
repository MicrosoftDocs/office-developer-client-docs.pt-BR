---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3f03412c9ab639678c68016ec1a8eff937b6c1a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590985"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gerencia formulários em bibliotecas de formulários. Esta interface é usado para criar bibliotecas de formulários do aplicativo específico. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de contêiner de formulário  <br/> |
|Implementada por:  <br/> |Provedores de biblioteca de formulário  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormContainer  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Instala um formulário em um contêiner de formulário.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Remove um determinado formulário de um contêiner de formulário.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Resolve uma classe de mensagem para o seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Resolve um grupo de classes de mensagens para seus formulários em um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulário.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Retorna o nome de exibição de um contêiner de formulário.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) contendo informações sobre o erro anterior que ocorrem ao objeto de contêiner do formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

