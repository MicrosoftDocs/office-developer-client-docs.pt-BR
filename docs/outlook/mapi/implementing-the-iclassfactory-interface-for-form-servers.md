---
title: Implementando a Interface IClassFactory para servidores de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767444"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementando a Interface IClassFactory para servidores de formulário

  
  
**Aplica-se a**: Outlook 
  
[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) é a interface OLE que aplicativos clientes usam para criar novos objetos de formulário da classe de mensagem do seu servidor de formulário. A tabela a seguir lista os métodos de **IClassFactory** necessários. 
  
|**Method**|**Descrição**|
|:-----|:-----|
|[CreateInstance](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |Cria um novo objeto de formulário.  <br/> |
|[LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |Protege o servidor de formulário na memória para que possa ser evitada sobrecarga de inicialização quando vários objetos de formulário são criados.  <br/> |
   
Para todas as informações necessárias para implementar esses métodos, consulte a seção Serviços de objetos ActiveX e COM no SDK do Windows.
  
## <a name="see-also"></a>Confira também



[Escrevendo códigos de servidor do formulário](writing-form-server-code.md)

