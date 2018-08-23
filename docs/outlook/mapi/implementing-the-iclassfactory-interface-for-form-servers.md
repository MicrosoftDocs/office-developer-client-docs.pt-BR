---
title: Implementar a Interface IClassFactory para servidores de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ff8766c6211d9820a2beed1fed871f82089b82fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566779"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementar a Interface IClassFactory para servidores de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) é a interface OLE que aplicativos clientes usam para criar novos objetos de formulário da classe de mensagem do seu servidor de formulário. A tabela a seguir lista os métodos de **IClassFactory** necessários. 
  
|**Method**|**Descrição**|
|:-----|:-----|
|[CreateInstance](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |Cria um novo objeto de formulário.  <br/> |
|[LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |Protege o servidor de formulário na memória para que possa ser evitada sobrecarga de inicialização quando vários objetos de formulário são criados.  <br/> |
   
Para todas as informações necessárias para implementar esses métodos, consulte a seção Serviços de objetos ActiveX e COM no SDK do Windows.
  
## <a name="see-also"></a>Confira também



[Gravar um código de servidor de formulário](writing-form-server-code.md)

