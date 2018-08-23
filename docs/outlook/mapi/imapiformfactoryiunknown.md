---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b2aa08ea14df87f24cda3da0137ae4bfa2c50b40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576012"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Suporta o uso dos formulários configuráveis de tempo de execução em ambientes de computação distribuídos. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de fábrica do formulário  <br/> |
|Implementada por:  <br/> |Servidores de formulário  <br/> |
|Chamado pelo:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormFactory  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Retorna um objeto de fábrica de classe do formulário.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto form fábrica.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Mantém um servidor de formulário aberto na memória.  <br/> |
   
## <a name="remarks"></a>Comentários

A interface **IMAPIFormFactory** baseia-se na interface [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) e objetos que implementam **IMAPIFormFactory** também devem herdar de **IClassFactory**.
  
 **IMAPIFormFactory** é a interface que os visualizadores de formulário usam para criar novos objetos de formulário quando um servidor de formulário oferece suporte a mais de uma classe de mensagem (ou seja, mais de um tipo de objeto do formulário). 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

