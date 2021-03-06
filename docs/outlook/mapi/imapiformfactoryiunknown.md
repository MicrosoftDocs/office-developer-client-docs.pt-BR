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
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342116"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oferece suporte ao uso de formulários de tempo de executar configuráveis em ambientes de computação distribuída. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Exposto por:  <br/> |Objetos de fábrica de formulário  <br/> |
|Implementado por:  <br/> |Servidores de formulário  <br/> |
|Chamado por:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormFactory  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Retorna um objeto de fábrica de classe para o formulário.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior ocorrendo no objeto de fábrica de formulário.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Mantém um servidor de formulário aberto na memória.  <br/> |
   
## <a name="remarks"></a>Comentários

A interface **IMAPIFormFactory** é baseada na interface [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) e os objetos que implementam **IMAPIFormFactory** também devem herdar **de IClassFactory**.
  
 **IMAPIFormFactory** é a interface que os visualizadores de formulário usam para criar novos objetos de formulário quando um servidor de formulário oferece suporte a mais de uma classe de mensagem (ou seja, mais de um tipo de objeto de formulário). 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

