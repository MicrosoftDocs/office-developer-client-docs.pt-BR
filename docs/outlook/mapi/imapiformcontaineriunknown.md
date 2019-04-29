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
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407526"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gerencia formulários em bibliotecas de formulários. Essa interface é usada para criar bibliotecas de formulários específicas de aplicativos. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
|Exposto por:  <br/> |Objetos contêiner de formulários  <br/> |
|Implementado por:  <br/> |Provedores de biblioteca de formulários  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormContainer  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Instala um formulário em um contêiner de formulários.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Remove um formulário específico de um contêiner de formulários.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Resolve uma classe de mensagem para seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para esse formulário.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Resolve um grupo de classes de mensagem para seus formulários em um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulários.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Retorna o nome de exibição de um contêiner de formulários.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto contêiner de formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

